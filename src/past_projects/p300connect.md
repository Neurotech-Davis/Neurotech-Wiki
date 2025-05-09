# P300 ERP Signal Excitation and Analysis

_Authors: Emma Chan, Alan Lin, Siri Manthapuri, Taner Karaaslan_

_Mentored by Avni Bafna, Adit Jain, Prakhar Sinha_

## Abstract

The OpenBCI Cyton board was used to extract EEG signals for data collection. The Cyton’s electrode placements are shown in Figures 1 and 3. These placements were chosen based on past P300 research conducted by Emmanuel Maby et al[1]. In each data collection trial, the test subject observed a colored LED that was set to white by default (as seen in Figure 2). Over a period up to 202.41 seconds, the LED's color would be changed at random times and then instantly reverted to the default color. This color change served as the target stimulus meant to trigger the P300. Each time a color change happened, a timestamp was marked. We conducted 5 data collection trials with 87 instances of P300 in total with two subjects.

Our data was then preprocessed and visualized using MNE-Python. During preprocessing, several filters were applied to the data: a bandpass filter with a band of 0.5-35 Hz and a 60 Hz notch filter. The bandpass filter served to increase the P300’s visibility in frequency-domain graphs. The notch filter served to filter out power line noise. Independent component analysis was then utilized to remove possible artifacts in the EEG data.

The P300 is an event related potential (ERP) that occurs approximately 300 ms after the presentation of sudden, unexpected stimuli. Our project aims to explore the P300’s human-computer interfacing capabilities by developing a P300-based Connect-4 brain-computer interface (BCI). To develop this BCI, several EEG data collection trials were conducted in which a test subject was presented with unexpected stimuli. From the collected data, the P300’s frequency was determined to be approximately 32 Hz. Peaks in the EEG data were observed approximately 300 ms after each presentation of unexpected stimuli thus verifying the P300’s presence. Our findings provide a body of data that can be used to develop a P300 classifier and a P300-based Connect-4 game.

## Introduction

The P300 relies on the oddball paradigm in which participants are presented with a common stimulus and then presented with a rare/target stimulus. The presentation of the rare stimulus is what triggers the P300. Research on P300 in BCIs has focused on leveraging this response to rare stimulus to enable user control, offering a direct pathway for communication and control through the interpretation of the brain's responses to specific stimuli. Our team aimed to utilize previous research on P300 and BCI user control to create a P300-based BCI that demonstrates the P300’s user control capabilities.
  
In our Connect-4 BCI design, participants focus on which column they would like to drop their piece into. Each column will flash and change into a different color. Once the participant’s column of focus changes color, the P300 is triggered, as the color change is the rare stimulus, which then alerts the computer to place a disk in the column of focus, essentially allowing for the game to be played only with the mind.

## Methods

- **Data Collection:**
  - **Hardware:** OpenBCI Cyton board for EEG signal collection
  - **Stimulus:** Colored LED that changes color to trigger P300
  - **Data Collection Trials:** 5 trials, 87 P300 instances, 2 subjects

- **Preprocessing:**
  - Bandpass filter (0.5–35 Hz) to enhance frequency resolution
  - 60 Hz notch filter to remove power line noise
  - Independent Component Analysis (ICA) for artifact removal
  - Visualization and preprocessing were performed using MNE-Python
 
## Results

Once we finished preprocessing the data and cleaning it up to prepare for feature extraction and classifier training, we generated graphs of the preprocessed data in time-domain and frequency-domain. A spike can be observed at around 32 Hz, which indicates the P300’s frequency.  A positive inflection can be observed at around 66.3s (one of the times the target stimulus was shown), thus indicating the presence of the P300. This data will be used later in classification and training the classifier.


## Conclusion

So far, we have been able to stimulate the P300 ERP using a light and collect the data via EEG sensors using the OpenBCI Cyton Board. We were then able to preprocess this data and epoch the data based on the timestamps indicating the occurrence of uncommon stimuli. Our future steps include developing a support vector machine classifier using the collected P300 data. Once the classifier has been trained, we will then develop a Connect-4 game. In this, we will be changing the colors of the columns through flashes of light, similar to the stimulus used during our data collection, to invoke the P300 ERP. Our classifier should then recognize this response and prompt the computer to put the disc in the player’s desired column, completing their move. We hope to accomplish this with the goal of ultimately having a setup where participants can play a simple game from their childhood with only their thoughts.
