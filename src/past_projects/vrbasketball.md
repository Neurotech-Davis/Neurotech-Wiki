# Controllerless Basketball Game using EEG-Based BCI: A Novel Approach for Virtual Reality Gaming 
> Mind Over Controllers—BCI-Powered Basketball for an Immersive Gaming Experience.

_Developed by Adit Jain, Priyal Patel, Rytham D, Sasinathaya Aphichatphokhin, Tarun Devesetti_

_Mentored by Prakhar Sinha, Maitri Khanna, Jordan Ogbu Felix_

This BCI project explored the intersection of gaming and neurotechnology by developing a controller-free basketball game, using EEG signals to detect jaw clenching for shooting mechanics—showcasing the potential of brain-computer interfaces in interactive entertainment.

## What it does

This BCI started off incredibly ambitious but generally started to scale back as they realized what was and what was not possible given the skillset and development time that they did. Originally, the group had aimed to develop a Unity game in VR and using different neurological signals in order to perform different actions in the game. However, as deadlines inched closer and closer, we realized that we would need to cut some corners on our ambition in order for the project to be completed on time. 

Their BCI project was centered around constructing a controller-less basketball game. The basic idea was for the user to shoot the ball by clenching their jaw and aligning the pointer with the basketball hoop. Utilizing EEG signals, the program was able to detect when a user clenches their jaw to trigger the shot in the game environment, while the duration of jaw-clenching controls the strength or distance of the shot. Later this was changed to just detecting jaw clenches in order to shoot the ball. 

OpenBCI EEG hardware was used to collect samples of jaw clench data to identify the range of frequencies needed to train the model to detect the user's jaw clenching. The electrodes are placed above the motor cortex area of the brain, based on previous research that identified this area as being involved in jaw clenching. 

Brainflow was used to parse the EEG signals and detect the desired stimuli in real-time. This BCI project offered an immersive and engaging gaming experience and was a really cool proof of concept to show what could be done with BCI’s. By using EEG signals to detect the user's jaw clenching, the game was able to respond in real time and it was a new and interesting look at the intersection between BCI’s and gaming. 
