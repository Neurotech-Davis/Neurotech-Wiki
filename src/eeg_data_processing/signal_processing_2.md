## What is Data Preprocessing?

Preprocessing refers to the procedure of removing noise and enhancing the signal of interest from the raw EEG data in order to get clean signals closer to the true neural activity. This helps transform raw data into a format that is suitable for analysis and extracting meaningful insights.

## Why is Preprocessing Needed?
* Signals picked up from the scalp are not an accurate representation of signals originating from the brain due to loss of spatial information.
* EEG data is very noisy as artifacts such as eye movements, cardiac activity, or muscle movements can distort the data which can obscure weaker EEG signals.
* It helps separate relevant neural activity from the random neural activity that occurs during EEG data recordings.

## How does Preprocessing differ based on the analysis?
Before beginning to preprocess the data, it is important to choose an appropriate method of preprocessing. Some relevant questions to keep in mind while preprocessing data are:
* What features of the EEG signal do you want to focus on?
If you are planning on analyzing whether the brain is in a relaxed state, you would analyze the alpha waves between 8-12Hz.
* What artifacts are present in the data? Which artifacts would you want to remove and which do you want to be aware of?
Artifacts like jaw clenches, eye movements, and muscle movements might be considered noise in some circumstances but could be helpful in revealing important patterns.

## Libraries used for Preprocessing:
* MNE (Magnetoencephalography and Electroencephalography) is an open-source Python library focused on processing and analyzing EEG and MEG data, offering tools for data preprocessing, visualization, source localization, and statistical analysis.
* Brainflow is an open-source library that provides a unified API for working with various EEG, EMG, and ECG devices, enabling developers to interact with neurophysiological data using a consistent interface.
