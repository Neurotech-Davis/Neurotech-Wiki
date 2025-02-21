# Expanding the P300 Oddball Paradigm for a Versatile BCI System with Macro Command Input
> Thought-Powered Coding—Exploring BCI for Seamless Vim Navigation.

_Developed by Devia Dham, Aurielle Jocom, Mathangi Venkatakrishnan, Raymond Kang_

_Mentored by Prakhar Sinha, Maitri Khanna, Jordan Ogbu Felix_

The P300 Macro Speller, developed for the 2023 Neurotech California Conference, aimed to revolutionize Vim navigation by detecting P300 brainwave responses, allowing users to switch modes and execute commands using thought alone—an ambitious project utilizing OpenBCI Cyton and Openvibe, with future potential for refinement.

## What it did

The P300 macro speller was a project that was in development to present at the 2023 Neurotech California Conference. It posed this simple question: “what if, instead of having to manually switch modes in Vim, we could think about them to reduce development time?”. The development of this project was sadly met with a few problems but it was a very interesting idea we hope to explore further in later years. 

This project is based on a well-established neurological phenomenon known as the P300 signal [could hyperlink to p300 article here]. This BCI would take advantage of these signals in order to detect when the user is thinking of a Vim command.

In their system, the stimuli are flashing lights presented on a screen, with the user focusing their attention on the desired stimulus to generate a P300 response. They expanded on this paradigm to allow for the selection of macros and commands, rather than just spelling out letters. This means that the user can input a range of commands, such as opening an application or initiating a specific action.

This project utilized the OpenBCI Cyton and Openvibe. Openvibe is meant to be an easy and accessible EEG recording and processing platform but it is also riddled with its own problems. The most prominent of these include many bugs while setting up and recording the EEG data. The most notable challenges faced by the group included having to wrestle with the Openvibe software to do what they wanted it to do. 
