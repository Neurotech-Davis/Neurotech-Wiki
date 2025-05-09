# Robotic Arm Movements BCI Controlled By EEG Mental Commands  
> Thought into Motion—Harnessing EEG to Control Robotic Limbs.

_Data Collection: Abrianna Johnson, Avni Bafna, Grace Lim_  
_Software and Hardware: Adit Jain, Ahmed Seyam, Evan Silvey, Prakhar Sinha, Priyal Patel_  

_Neurotech@Davis, University of California, Davis, CA_

This BCI project uses EEG signals to decode mental commands—such as “grab,” “drop,” “left,” and “right”—and converts them into real-time physical movements of a robotic arm. Leveraging mental imagery primed by video stimuli and personalized training sessions, the system enables direct control of robotic hardware through thought alone.

## What it does

This brain-computer interface enables users to control a robotic arm using non-invasive EEG technology. The system is designed to interpret distinct mental commands based on motor imagery and emotional arousal, translating them into specific actions of a robotic hand.

To achieve this, the team developed four core commands:
- **Grab:** Triggered by imagining a slow, deliberate phone lift.
- **Left:** Stimulated by envisioning a water bottle moving leftward.
- **Right:** Evoked using a fast, high-arousal stabbing motion with a pen.
- **Drop:** Prompted by visualizing a cartoon piano dropping from above.

Each mental command was paired with a priming video to elicit the intended neural response. During training, subjects reviewed these stimuli, spent a few seconds forming the associated mental image, and then entered a focused recording phase. They could accept or reject each session depending on their confidence in task execution. A “neutral” state served as the baseline, where subjects consciously refrained from mental imagery. Commands were introduced incrementally, allowing users to train each command independently and build familiarity before progressing.

## How it works

The system relies on rhythmic EEG patterns and motor-related mental imagery, likely utilizing mirror neuron activation. A subject-specific baseline was created using the neutral state. All EEG data were collected from consistent electrode channels on the EMOTIV Insight headset. The trained commands were individualized to each subject’s neural patterns and mapped to robotic movements.

## Results / Conclusion

Mental commands were detected in real-time using Emotiv’s software integrated with the Node-Red toolbox. A thresholding mechanism (initially ranging from 70–90) helped filter noise and validate signal strength, with each command producing a specific integer output:
- **1:** Grab  
- **2:** Drop  
- **3:** Left  
- **4:** Right  

These values were relayed via serial connection to an Elegoo UNO R3 microcontroller programmed through the Arduino IDE. The microcontroller activated specific servo motors controlling a 3D-printed robotic hand. Using a pulley system with fishing line, the servo motors applied tension to mimic finger and wrist movements in response to the user’s thoughts.

This project demonstrates a novel approach to assistive technology, showcasing the feasibility of thought-controlled robotics using affordable EEG hardware and customized training workflows.
