# BrainBeats – An EEG-Based Music BCI for Enhanced Focus
> Personalized Study Soundtracks—Decoding Focus with EEG and Machine Learning.

_Developed by Dara Banaie, Nidhi Vadulas, Britney Nguyen, Gautham Sivakumar, Devansh Vora_  
_Mentored by Prakhar Sinha, Avni Bafna, Adit Jain, Dhruv Sangamwar, Aryaman Bhatia_  

---

## Introduction

College students are constantly found with earbuds or wireless headphones as they do everything from walk to class to study for a final exam. Due to this extensive influence on students’ lives, we decided to see if various music genres can influence academic performance. There are contrasting views on whether music is beneficial for students. On one hand, some claim that music can improve the longevity of memory, enhance comprehension, and reduce anxiety. Studies have shown that distinct patterns of neural activity are associated with attentional states, with music facilitating those states. However, listening to music while trying to learn is also deemed as distracting and counterproductive. It is important to ask whether that applies to all genres of music and to all students equally. We believed that this question was worth exploring to discover and develop good study habits for ourselves as well as our peers.

---

## Objectives

- Understand which genre(s) of music, if any, promote focus and help concentration.  
- Study the converse—see which genres of music, if any, might negatively impact focus.  
- Inform participants on which genre of music is the most beneficial for their academic performance.  
- Help students make informed decisions on which genres of music to listen to while completing focus-related tasks and which to avoid.  
- Develop personalized playlists that help users stay focused by analyzing their performance and making genre suggestions in real-time.  

---

## Experimental Methods

Our selected music genres included classical, jazz, ambient, and lofi. Each genre was played for 10 minutes per participant, totaling 40 minutes of data collection per person.  
There were 7 participants in total. Each participant worked on homework or studied while listening to music and had their data collected.  
Data was collected using the OpenBCI Focus Widget, which recorded time spent concentrating based on EEG signals.  

---

## How the Model Works

Our project utilizes EEG data collected from participants to classify their focus states while listening to different music genres. Generating alpha and beta waves, we calculated a focus value from the EEG readings. We employed a Support Vector Machine (SVM) classifier to process EEG data and focus values.  

The model discerns whether participants are in a focused or unfocused state based on features extracted from EEG recordings, specifically Alpha and Beta wave power.  

---

## Type of Model

We used a Support Vector Machine (SVM) classifier for our task. SVMs are highly effective for high-dimensional data and for finding an optimal hyperplane that separates two classes—in our case, focused vs. unfocused.

### Parameters

Key parameters include:
- **C (Regularization Parameter)**: Balances the trade-off between maximizing the margin and minimizing classification error.
- **Kernel Function**: Determines the flexibility of the decision boundary. Options considered included linear, polynomial, and radial basis function (RBF) kernels.

---

## Inputs and Outputs

- **Inputs**: Features extracted from EEG data (specifically Alpha and Beta wave power from FFT amplitudes).
- **Output**: Binary classification indicating focused or unfocused state.

---

## Prediction of Overall Focus per Genre

Following classification of focus states, we aggregated the predictions to determine overall focus by genre for each participant. By analyzing these distributions, we identified the music genre that best facilitated focus for each individual. This insight helps recommend personalized music playlists tailored to enhance concentration and productivity.

---

## Results and Analysis

Our data showed that lofi was the most successful at eliciting concentration among participants, while jazz was the least. While lofi was consistently helpful for most participants, others responded better to ambient or classical music. These differences suggest that music preferences and effectiveness are highly individual.  

Several confounding factors may have influenced our results. Participants chose their own tasks, which might have varied in difficulty or familiarity. Prior experience listening to music while studying could also have affected how they processed music as a stimulus.

---

## Summary & Future Directions

Our study highlighted the potential of EEG-based BCI systems to guide students toward personalized music choices that enhance focus.  
**Future steps include:**
- Expanding the dataset with more participants.
- Incorporating additional music genres (e.g., pop, frequency tones).
- Developing real-time applications that interpret EEG data and recommend music dynamically.
- Exploring EEG-based detection of other cognitive states like relaxation or motivation.

By combining neuroscience and machine learning, BrainBeats offers a unique approach to improve academic performance through brain-driven music personalization.
