# Setting-Up the Environment

By Avni Bafna for Neurotech@Davis

Before starting preprocessing import and install the dependencies.
```
import pandas as pd
import numpy as np
!pip install mne
import mne
```

## Load the raw data and plot the data file
* Import the raw EEG data from the recording equipment (OpenBCI data file) into your analysis software (Jupyter notebook) and plot the data.
* Verify that the sampling rate is appropriate for your analysis. Common EEG sampling rates are 250 Hz or 500 Hz. 

```
# Load CSV data using pandas
csv_file_path = '/content/drive/MyDrive/Sample/BrainFlow-RAW.csv'

# Load data from CSV into an array
trial_data = np.genfromtxt(csv_file_path)

# Declares channel names and types of each set of data
sfreq = 250  # sample rate in Hz
ch_names = ['Channel {}'.format(i) for i in range(trial_data.shape[1])]
ch_types = ['eeg' for i in range(trial_data.shape[1])]

# Create info structures and RawArray objects for each set of data
info = mne.create_info(ch_names=ch_names, sfreq=sfreq, ch_types=ch_types)
raw = mne.io.RawArray(trial_data.T, info)

# Removing irrelevant channels
ch_names = [raw.ch_names]
ch_names_to_keep = [ch_names[0][1:9]]
raw = raw.pick_channels(ch_names_to_keep[0])

# Now you can work with the MNE Raw object
print(raw.info)
print(raw.get_data())

# Plot the specified interval
raw.plot(duration=200, scalings='auto')
```

## Filtering
It is common to filter certain frequencies so that we can enhance the frequencies of interest.
### High-Pass Filter:
* A high-pass filter attenuates frequencies below a certain cutoff frequency and allows higher frequencies to pass through.
* In EEG preprocessing, a high-pass filter is used to remove slow variations, DC offsets, and other low-frequency artifacts, such as electrode drift or baseline shifts.
* Common cutoff frequencies for high-pass filters in EEG data preprocessing are around 0.5 Hz.

```
# Apply a high-pass filter with a cutoff frequency of 3 Hz
raw.filter(l_freq=3, h_freq=None)
raw.plot(duration=200, scalings='auto')
```

### Low-Pass Filter:
* A low-pass filter attenuates frequencies above a certain cutoff frequency and allows lower frequencies to pass through.
* In EEG preprocessing, a low-pass filter helps remove high-frequency noise, muscle artifacts, and high-frequency components that are not relevant to the analysis.
* Common cutoff frequencies for low-pass filters in EEG data preprocessing are typically around 40 Hz.

```
# Apply a low-pass filter with a cutoff frequency of 40 Hz
raw.filter(l_freq=None, h_freq=40)
raw.plot(duration=200, scalings='auto')
```

### Band-Pass Filter:
* A band-pass filter allows a specific range of frequencies, defined by a lower cutoff frequency and an upper cutoff frequency, to pass through while attenuating frequencies outside this range.
* In EEG analysis, a band-pass filter is often used to isolate frequency bands of interest, such as alpha (8-13 Hz), beta (13-30 Hz), or gamma (30-100 Hz), which are associated with different cognitive processes.
* Band-pass filters are useful for extracting features and patterns specific to certain frequency ranges.

```
# Apply a bandpass filter with cutoff frequencies of Alpha waves between 8 Hz (low) and 13 Hz (high)
raw.filter(l_freq=8, h_freq=13)
raw.plot(duration=200, scalings='auto')
```

### Notch Filter (Band-Cut Filter):
* A notch filter, also known as a band-cut filter that removes a single frequency.
* Notch filters are used to remove specific sources of interference, such as power line noise (50 or 60 Hz) and their harmonics, which can contaminate EEG signals.
* Notch filters help eliminate periodic noise sources that might be present due to electrical interference.

```
# Apply a notch filter to remove 60 Hz line noise
raw.notch_filter(60)
raw.plot_psd(fmin=2, fmax=80);
```

## Artifact Removal and Correction
Artifacts can distort the EEG signal and interfere with accurate analysis and interpretation. There are various types of artifacts, including eye blinks, muscle movements, electrode noise, and external interference.
### Artifact Detection:
- Automatic Detection: Automated algorithms, such as independent component analysis (ICA), wavelet decomposition, or template matching, can identify components or segments that deviate significantly from the expected EEG patterns. These algorithms often require training data or templates to differentiate artifacts from brain activity.
- Manual Detection: Visual inspection by experts involves reviewing EEG data to identify visually apparent artifacts, such as sharp spikes, slow drifts, or sudden jumps in signal amplitude.
### Artifact Removal:
- Independent Component Analysis (ICA): ICA is a widely used method that separates EEG data into independent components, some of which might represent artifacts. By manipulating these components, unwanted artifacts can be removed or minimized while preserving genuine brain-related components.

```
from mne.preprocessing import ICA
num_components = 6 #play around with this number to get components that seem to represent the actual brain activations well
ica = ICA(n_components=num_components, method='fastica')
ica.fit(raw)

raw.plot(scalings='auto')
```

- Regression-Based Methods: Regression techniques can be used to model and remove artifacts by regressing out the artifact's contribution from the EEG signal. For instance, electrooculogram (EOG) channels can be used to regress out eye movement artifacts.
- Interpolation: If an entire electrode or channel is affected by an artifact, interpolation techniques can be employed to estimate and replace the missing or distorted data based on neighboring electrodes.
### Specialized Techniques:
- Muscle Artifact Removal: Muscle artifacts can be removed by incorporating electromyogram (EMG) recordings or by applying high-pass filters to suppress low-frequency muscle activity.
- Eye Blink Artifact Removal: Eye blink artifacts can be detected and corrected using EOG channels. These artifacts can be identified by the characteristic shape of EOG signals during eye movements.
 
## Removing bad channels
EEG data might contain ‘bad’ channels that do not provide accurate information and it is important to remove them from the analysis.
A channel might be excluded if:
- The electrode was placed improperly or had poor contact with the scalp.
- The channel malfunctioned.

By visualizing the raw data, we can identify ‘bad’ channels that have no signal or look noisier than other channels.
After identifying the bad channels, we can exclude them from the analysis by creating a subset of channels marked as ‘bad’.
An optional step would be to interpolate (fill in the missing data) by using the activity of surrounding channels to make an educated guess of activity at the bad channel.

```
# Mark channels as bad
bad_channels = ['Channel 2', 'Channel 6']  # List of channel names to mark as bad
raw.info['bads'] = bad_channels

# Remove bad channels from further analysis
raw.pick_types(eeg=True, exclude='bads')

# Plot the cleaned EEG data
raw.plot(scalings='auto')
```

## Downsampling (optional)
Downsampling is the process of reducing the sampling rate of a signal by selecting and keeping only a subset of the original samples.
This is typically done to reduce computational load, storage requirements, and to focus on specific frequency components of interest.
Downsampling can also result in loss of high-frequency information and introduce aliasing effects if not performed carefully with appropriate anti-aliasing filters.
 
## 3.6 Re-referencing (optional)
Re-reference the data to a common point of reference if it was initially referenced to individual electrodes.
References should be located as far away from the signal of interest (ie. Mastoid, earlobe)
