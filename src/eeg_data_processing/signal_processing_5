## What is feature extraction?

Feature extraction is a process in which meaningful and informative attributes or features are derived from raw data. In the context of EEG (electroencephalography) data analysis, feature extraction involves transforming the complex EEG signal into a set of representative features that capture essential characteristics of brain activity. These extracted features serve as inputs for further analysis, classification, and interpretation.

## Why is feature extraction important?
- Dimensionality Reduction:
EEG data can consist of hundreds or thousands of data points (channels) collected over time. Extracting relevant features condenses this high-dimensional data into a smaller set of informative attributes, reducing computational complexity and memory requirements.
-  Information Compression:
 Feature extraction condenses raw EEG signals into meaningful representations that capture essential characteristics of brain activity. This compression retains important information while discarding noise and irrelevant details.
- Machine Learning:
Many machine learning algorithms work better with lower-dimensional feature sets. Well-chosen features can improve the performance of algorithms by providing them with more relevant information.
- Statistical Significance:
Extracted features can be used as input to statistical tests, making it easier to analyze and compare data between different conditions or groups.
Depending on the research question, you can tailor feature extraction to focus on specific aspects of the EEG data, such as frequency content, temporal patterns, or connectivity.

## Methods of feature extraction
- Manual Feature Extraction:
Manual feature extraction involves selecting and computing features from data based on domain knowledge and expertise. Researchers identify relevant attributes by understanding the underlying phenomena and selecting features that are informative for the analysis. This approach requires a deep understanding of the data and its context, as well as expertise in signal processing and neuroscience. Manual feature extraction can lead to highly interpretable and domain-specific features, but it can be time-consuming and might not capture all subtle patterns in complex data.
- Automatic Feature Extraction:
Automatic feature extraction employs algorithms to automatically identify relevant features from raw data. These algorithms learn from the data itself and capture patterns that might not be immediately apparent to humans. Techniques such as deep learning, wavelet transforms, and principal component analysis (PCA) are used to extract features without manual intervention. Automatic methods can efficiently handle high-dimensional data, uncover intricate patterns, and be more robust to noise. However, they might produce features that are less interpretable than those obtained through manual extraction.

## Event Related Potential
Event-related potentials (ERPs) are small, rapid fluctuations in the electroencephalogram (EEG) signal that occur in response to specific sensory, cognitive, or motor events. ERPs are time-locked to the onset of these events and provide valuable insights into the brain's neural processing of different stimuli or conditions. ERPs are widely used in neuroscience, cognitive psychology, and clinical research to study the timing, amplitude, and topography of brain responses to various stimuli or tasks.
Some examples of ERPs are:
- P300 (Oddball Paradigm):
In an oddball paradigm, participants are presented with a series of stimuli, most of which are common (frequent), and some are rare (infrequent or deviant).
The P300 ERP is a positive deflection in the EEG waveform that occurs around 300 milliseconds after the presentation of a rare or target stimulus.
P300 is associated with attention, cognitive processing, and the detection of significant or unexpected events.
- N170 (Face Recognition):
The N170 ERP is a negative deflection occurring around 170 milliseconds after the presentation of faces or other visually complex stimuli.
N170 is particularly pronounced when participants are presented with faces compared to other object categories.
It reflects early visual processing and is often associated with face perception and recognition.
- Mismatch Negativity (MMN):
MMN is a negative ERP component that occurs when participants are presented with an unexpected or deviant stimulus in a sequence of standard stimuli.
It appears around 100-250 milliseconds after the presentation of the deviant stimulus.
MMN is related to the brain's automatic detection and processing of auditory changes and can be used to study sensory memory and cognitive processes.
- N400 (Language Processing):
The N400 ERP is a negative deflection occurring around 400 milliseconds after the presentation of a semantically incongruent word or phrase within a sentence.
It reflects semantic processing and is sensitive to violations in the meaning or context of language.
- Contingent Negative Variation (CNV):
CNV is a slow, negative-going potential that emerges during the anticipation of an upcoming event or stimulus.
It is often used in studies involving temporal expectations and preparation for motor responses.
- Error-Related Negativity (ERN):
ERN is a negative deflection that occurs shortly after an individual makes an error during a cognitive task.
It is thought to reflect the brain's detection of errors and is associated with conflict monitoring and response inhibition.

## 5.5 Feature Extraction Techniques
- Principal component analysis, or PCA, is a dimensionality-reduction method that is often used to reduce the dimensionality of large data sets, by transforming a large set of variables into a smaller one that still contains most of the information in the large set.
- ICA is a statistical procedure that splits a set of mixed signals to its sources without previous information on the nature of the signal. The only assumption involved in the ICA is that the unknown underlying sources are mutually independent in statistical terms. ICA assumes that the observed EEG signal is a mixture of several independent source signals coming from multiple cognitive activities or artifacts.
- Locally linear embedding (LLE) seeks a lower-dimensional projection of the data which preserves distances within local neighborhoods. It can be thought of as a series of local Principal Component Analyses which are globally compared to find the best non-linear embedding.
- t-SNE ( t-Distributed Stochastic Neighbor Embedding) is a technique that visualizes high dimensional data by giving each point a location in a two or three-dimensional map. The technique is the Stochastic Neighbor Embedding (SNE) variation that is much easier to optimize and produces significantly better visualization.

## Fourier Transform
Fourier Transform is a mathematical technique used to analyze and transform a signal from its original time domain representation into its frequency domain representation. In the context of EEG (electroencephalography), the Fourier Transform is used to understand the frequency components present in the EEG signals, revealing information about the underlying neural activity.
- Time Domain to Frequency Domain:
EEG signals are originally recorded as a series of voltage measurements over time. The Fourier Transform converts these time-domain EEG signals into a representation that shows how much energy is present at different frequencies.
- Components of Fourier Transform:
The Fourier Transform decomposes the EEG signal into a sum of sinusoidal waves (sine and cosine functions) of different frequencies and amplitudes.
Each component in the sum represents a specific frequency component within the original EEG signal.
- Frequency Spectrum:
The output of the Fourier Transform is a frequency spectrum, which is a plot of frequency on the x-axis and the corresponding magnitude or power of each frequency component on the y-axis.
The spectrum shows which frequencies are present in the EEG signal and how strong they are.
- Dominant Frequency Bands:
EEG signals typically contain multiple frequency components, which can be categorized into different frequency bands: delta (0.5-4 Hz), theta (4-8 Hz), alpha (8-13 Hz), beta (13-30 Hz), and gamma (30-100 Hz).
Analyzing the power distribution across these frequency bands can provide insights into the brain's activity during different cognitive states.
- Power Spectral Density (PSD):
The power spectral density is a measure of how the power of each frequency component in the EEG signal is distributed across the frequency spectrum.
The PSD provides information about the relative strength of different frequency bands, allowing researchers to identify dominant frequencies and trends in brain activity.
