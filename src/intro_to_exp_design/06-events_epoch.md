# Event Codes and Epoching
By Grace Lim for Neurotech@Davis

### Event Codes

As you may know, the most important property of EEG comes from its temporal resolution. This is why the creation of event codes, an integer that indicates the type of event that occurred during data collection and the time it happened, is crucial. The actual number that denotes an event is arbitrary, but it is important that you use a different integer for each event. Some examples of events you might want to create a code for are: the onset of your target stimulus or the onset of the participant’s response. The reason event codes are important is to create epochs and makes it possible to analyze how brain activity is related to particular stimuli or actions. 

| Event              | Description                               | Event Code |
|--------------------|-------------------------------------------|------------|
| Valid Target       | A correctly identified target stimulus    | 100        |
| Invalid Target     | An incorrectly identified target          | 101        |
| Non-Target         | A non-target stimulus                     | 200        |
| Correct Response   | Participant responds correctly            | 300        |
| Incorrect Response | Participant responds incorrectly          | 301        |
| No Response        | Participant fails to respond              | 400        |

This table here I just created from ChatGPT to show a simple event code table for a hypothetical experiment. You can see here how related events have similar event codes, which is just a stylistic choice. 

Whoever is programming the stimuli can create a script to send these event codes to the EEG recording system. These event codes will pop up in real time as you run your experiment, so you can use this information for analysis.

For more information on event codes, please visit [here](https://socialsci.libretexts.org/Bookshelves/Psychology/Biological_Psychology/Applied_Event-Related_Potential_Data_Analysis_(Luck)/02%3A_Processing_the_Data_from_One_Participant_in_the_ERP_CORE_N400_Experiment/2.03%3A_Exercise_-_Looking_at_the_EEG_and_the_Event_Codes) or the [ERPLAB wiki page](https://github.com/ucdavis/erplab/wiki/ERPLAB-Studio-Tutorial)

### Epoching

Epoching is the process of converting the continuous EEG to time-locked segments that correspond to your events. This is interrelated to event codes because you use your event codes to create epochs surrounding them. For example, an epoch might start 200 milliseconds before the stimulus and end 800 milliseconds after it. These epochs are then averaged into bins, so we can identify patterns in our neural data in response to events. Bins are just containers of epochs that are using the same event, this is arbitrary as one can make these conditions very specific. Different experimental conditions (e.g., valid vs. invalid targets) generate separate sets of epochs, allowing comparisons of brain activity across different types of stimuli or responses. Epochs are typically used in ERP experiments because of the nature of averaging ERPs found across trials or bins. However, as you read more on different types of EEG experiments you will find how crucial event codes and epoching are. 

For more information on epoching, in the more practical sense, please visit the [ERPLAB wiki page](https://github.com/ucdavis/erplab/wiki/ERPLAB-Studio-Tutorial). If you are not using EEGLAB in MATLAB I recommend researching the documentation for a Python based library.
