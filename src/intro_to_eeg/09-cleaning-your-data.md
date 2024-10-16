# Cleaning your data
When you have finally collected all your data, your data will consist of both EEG data and unwanted electrical data not related to your experiment. This could include things such as electrical signals from lights and computers, eye blinks, muscle activity, etc. which are unrelated to your experiment. These are called artifacts.

![artifacts](https://i.postimg.cc/9z3Gp1dm/Screenshot-2024-09-19-at-5-02-51-PM.png)

It is important to get rid of these as they can cause unwanted peaks and distortions to your data, make it unreliable to find the actual ERP from your experiment.

There are two methods for dealing with artifacts: artifact rejection and artifact correction. Artifact rejection involves identifying and removing segments of data that contain artifacts. Artifact correction attempts to remove the artifact while preserving the underlying neural signal. There are multiple ways to do this, and one that has been discussed below is Independent Component Analysis. There are other methods which have been linked.

## Blinks

A very common artifact is blinking. Each eye has a constant electrical potential between the cornea and the retina. The voltage recorded from electrodes near this site are called electrooculogram, or EOG as you may see labelled in MNE. When the subject blinks, this potential is changed, causing the artifact.

Blinking is also a good way to make sure your headset is recording data. Tell your subject to blink rapidly, and some very obvious deflections should occur. You can also do jaw clenches.

![blink1](https://i.postimg.cc/CKjLB71C/Screenshot-2024-09-19-at-5-04-00-PM.png)
![blink](https://i.postimg.cc/Y0XS2SSJ/Screenshot-2024-10-15-at-6-10-44-PM.png)

Blink potentials are such that they have negative polarity under the eye, and positive polarity over the eye. Here, you can see the negative polarity in the vertical EOG and see the difference between a blink and not a blink.

![blink3](https://i.postimg.cc/t49HvbC6/Screenshot-2024-09-19-at-5-04-31-PM.png)

Since there is a clear negative polarity, one method of removing these artifacts is to conduct two separate recordings, one with the electrode below the eye and one above. You can then subtract the lower -minus the upper (lower - upper) and see the eye blink to see them even more clearly.

In MNE, you can also use the functions create_eog_epochs() which takes the artifacts and puts them into epochs. You may need to fine tune the functions parameters before using it, so be sure to have a look at the documentation in case you don’t. https://mne.tools/stable/auto_tutorials/preprocessing/10_preprocessing_overview.html#ocular-artifacts-eog

## Eye movements

As in eye blinks, eye movements also result from the dipole in the eye. The front of your eye has positive charge. When you turn to a certain direction, positive charge gets accumulated in that part of the face, and negative on the other side. 

![eye move](https://i.postimg.cc/GtBp2Cst/Screenshot-2024-09-19-at-5-05-06-PM.png)

In general, eye movements show a sharp movement deflection in the waveform and then back to original position as below. HEOG stands for horizontal eog.

![eye move2](https://i.postimg.cc/7LdHWRRy/Screenshot-2024-09-19-at-5-05-30-PM.png)

You can also use the create_eog_epochs() function in MNE. Again, make sure to see if you need to fine tune the function before using it. https://mne.tools/stable/auto_tutorials/preprocessing/10_preprocessing_overview.html#ocular-artifacts-eog

## Low voltage drifts

Low voltage drifts are caused by small movements in the position of the electrode, which can be due to the subject moving during the experiment or sweat. The change in movement causes impedance to change, leading in sustained shift in voltage.

It often looks something like this, and can be detected by visual inspection

![low voltage drift](https://i.postimg.cc/FRCj8h4H/Screenshot-2024-09-19-at-5-18-43-PM.png)

![low voltage 2](https://i.postimg.cc/QtD8D7j6/Screenshot-2024-09-19-at-5-19-00-PM.png)

It’s a good idea to zoom out in your program and observe these drifts. You can remove these by applying a high pass filter and making sure the subject does not move much during the experiment. (Normally 0.1Hz, but may be subject to change based on your data)

## Power line noise

For detecting power line noise, first convert your data into frequency domain. Then, notice if there is any large spike at the 60Hz mark. Apply filter to remove this. EZ

## Muscle and heart activity
Muscle and heart activity can create significant artifacts in EEG recordings. Muscle artifacts are typically caused by tension in facial or neck muscles, which can produce high-frequency noise in the EEG signal. These artifacts are often characterized by sudden, sharp spikes or sustained periods of high-frequency activity.

Heart activity, particularly the QRS complex of the heartbeat, can also introduce artifacts into EEG recordings. These are known as electrocardiogram (ECG) artifacts and appear as regular, rhythmic spikes in the EEG data.

Speech can also create artifacts due to the movement of facial muscles and changes in skull pressure. These artifacts are often more complex and can vary based on the individual and the type of speech.

To detect and remove these artifacts, MNE-Python provides several functions. For muscle artifacts, you can use create_eog_epochs() or create_ecg_epochs() to identify epochs containing these artifacts. For heart-related artifacts, the find_ecg_events() function can be useful. These functions help in identifying and potentially removing segments of data contaminated by muscle and heart activity.

It's important to note that while these artifacts can be problematic, they also contain valuable physiological information. Therefore, careful consideration should be given to the balance between artifact removal and preservation of relevant neural activity.


## Independent Component Analysis (ICA)

Independent Component Analysis (ICA) is a powerful technique used in EEG data processing to separate and remove artifacts from the signal. It's particularly useful for dealing with complex artifacts that are difficult to remove using simple filtering methods.

Here's how ICA works in the context of EEG data cleaning:

1. Decomposition: ICA decomposes the EEG signal into statistically independent components. Each component represents a source of activity, which could be brain activity or an artifact.
2. Identification: After decomposition, components that represent artifacts (e.g., eye movements, muscle activity, or heartbeats) are identified. This can be done manually by visual inspection or using automated methods.
3. Removal: The identified artifact components are then removed from the data.
4. Reconstruction: Finally, the cleaned EEG signal is reconstructed using the remaining components.

ICA is particularly effective for removing ocular artifacts (like eye blinks and movements) and can also help with other types of artifacts that have consistent spatial patterns.

In MNE-Python, you can perform ICA using the mne.preprocessing.ICA class. Here's a basic example of how to apply ICA:

```python
from mne.preprocessing import ICA

# Create ICA object
ica = ICA(n_components=20, random_state=97)

# Fit ICA
ica.fit(raw)

# Plot ICA components
ica.plot_components()

# Apply ICA to the raw data
raw_clean = ica.apply(raw)
```

Other methods include: 

https://mne.tools/stable/auto_tutorials/preprocessing/35_artifact_correction_regression.html

https://mne.tools/stable/auto_tutorials/preprocessing/50_artifact_correction_ssp.html