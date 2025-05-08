# NeuroBird: Using Steady-State Visually Evoked Potentials to Guide a Drone

**Team Members:** Alex Czerminski, Angelina Gyves, Sofia Fischel, Anthony Noshy, Priyanshi Singh, Shreya Vallala  
**Advisors:** Avni Bafna, Adit Jain, Prakhar Sinha  

## Project Description

**NeuroBird** is a brain-computer interface (BCI) project that enables hands-free control of a drone using Steady-State Visually Evoked Potentials (SSVEPs), which are brain responses triggered by flickering visual stimuli. The system leverages two screens, each flickering at a distinct frequency—5Hz (left) and 7.5Hz (right)—to steer the drone left or right based on where the user focuses their gaze.

A live video feed from the drone is displayed on a tablet, allowing the user to navigate through an obstacle course in real time. EEG electrodes placed at the O1 and O2 locations on the scalp capture the brain’s response to the visual stimuli. These signals are then analyzed to detect which frequency dominates, indicating the user's intended direction.

Though initial trials showed inconsistent results due to noisy signals and timing issues with the CytonBoard, future iterations aim to refine data collection and employ a K-Nearest Neighbors (KNN) classifier to distinguish between left, right, and forward commands. Ultimately, classified brainwave patterns are translated into drone movement using the Tello Drone API.

This project demonstrates a novel method of integrating real-time brain signal interpretation with autonomous drone navigation using consumer-grade EEG hardware.
