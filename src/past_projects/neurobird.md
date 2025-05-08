# The NeuroBird: Using Steady-State Visually Evoked Potentials to Guide a Drone  
> Brainwaves Take Flight—Controlling Drones with the Power of Sight.

_Developed by Alex Czerminski, Angelina Gyves, Sofia Fischel, Anthony Noshy, Priyanshi Singh, Shreya Vallala_

_Mentored by Avni Bafna, Adit Jain, Prakhar Sinha_

This BCI project explored the use of Steady-State Visually Evoked Potentials (SSVEPs) to guide a drone through user intent. By leveraging EEG technology and live visual stimuli at two flashing frequencies, the drone was directed left or right through an obstacle course, making neuro-powered flight a reality.

## What it does

The NeuroBird leverages distinct SSVEP responses elicited by two separate flashing frequencies to direct a drone in real-time. Participants view a live video feed from the drone on a tablet while facing two screens that flash at 5 Hz (left) and 7.5 Hz (right). Based on the frequency that matches the participant's visual focus, the drone receives directional input to move left or right accordingly.

The system was designed to make navigation intuitive—simply by focusing on one screen or the other, the user influences the drone’s direction, creating a seamless interaction between brain activity and aerial robotics.

## How we built it

Participants sat in front of two monitors showing flickering lights at fixed frequencies. Electrodes were placed at O1 and O2—locations responsible for processing visual stimuli. Additional electrodes were placed on the frontal lobe and ear lobes to provide reference and control data.

Three key trials were conducted:

- **Trial A**: Establish baseline SSVEP responses between left (5 Hz) and right (7.5 Hz) stimuli.
- **Trial B**: Repeat with participants occasionally glancing up at the live drone feed on a tablet.
- **Trial C**: Assess noise introduced by the video stream’s own flicker effect to determine interference.

Each of the four participants completed five iterations of each trial, helping identify trends in SSVEP response behavior under varying conditions.

## Background

The brain's visual cortex responds to flickering visual stimuli with steady electrical patterns known as Steady-State Visually Evoked Potentials (SSVEPs). These responses are stable and occur at the same frequency as the visual input, making them ideal for non-invasive BCI applications.

SSVEPs are a subset of event-related potentials (ERPs), where repeated visual stimulation leads to predictable, periodic brain responses. Detecting these patterns via EEG allows us to interpret user intent purely through eye gaze and focus.

## Results & Conclusion

Despite preprocessing, the initial trials did not consistently yield clear SSVEP peaks, as illustrated in Fig. 5. One instance of Trial B showed a potential spike at 5 Hz (Fig. 6), but reproducibility remained a challenge.

We suspected inaccuracies in frequency mapping due to temporal drift in our CytonBoard, prompting a refinement of our data collection protocol. The updated trials involved direct exposure to each frequency (5 Hz and 7.5 Hz) for 30 seconds without interference.

Next steps involve integrating a K-Nearest Neighbors (KNN) classifier to categorize EEG data into left, right, or forward commands. These classifications will be translated into real-time drone commands using the Tello Drone’s API, enabling autonomous, brain-driven drone navigation.

This project showcases the potential of EEG-based BCI systems in real-world applications and paves the way for future innovations in hands-free, vision-driven technology.
