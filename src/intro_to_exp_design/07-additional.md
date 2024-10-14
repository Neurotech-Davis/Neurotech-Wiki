# Additionl Considerations
By Sofia Fischel for Neurotech@Davis

### ***SOA***

Stimulus-onset asynchrony, or SOA, is the length of time between the onset of one stimulus and the next. 

Determining the specific length of SOAs requires a certain threading of the needle. If the interval between stimuli is too long, subjects may grow fidgety, increasing EMG noise. In the context of ERP experiments, at “short SOAs, the brain will still be busy processing the first target when the second target appears, and this delays the response to the second target” (Luck). Note: a component that is highly refractory will, when “a stimulus at a particular location is preceded by another stimulus at the same location at a short delay,” produce a greatly reduced response to the second stimulus reduced” (Luck). Investigate the refraction period of the component, if applicable, and plan the SOA length accordingly. It is best to keep SOAs consistent across potential conditions, as a “degree of anticipation” may “confound the results” (Luck) if it varies across trial blocks.

For a more in depth explanation of this trade off, read page 144-5 from Luck, 2014.

> You will usually want to choose a stimulus duration that avoids offset responses, either by choosing a duration that is so short that it doesn’t produce a substantial offset response (e.g., 100 – 200 ms for visual stimuli) or is so long that the offset response occurs after the ERP components of interest (e.g., 1000 ms). In behavioral experiments, it is common for the stimulus to offset when the subject makes a behavioral response to the stimulus. … My typical approach for experiments with simple visual stimuli is to use a duration of 100 ms for college student subjects … For simple auditory tones, I would typically use a duration of 50 – 100 ms, including 5-ms rise and fall times. For experiments with more complex auditory or visual stimuli, I typically use a duration of 750 – 1000 ms.
> 

> Determining the optimal amount of time between trials requires balancing several factors. On the one hand, you want to keep the amount of time between trials as short as possible to get the maximal number of trials in your experimental session, thereby maximizing the signal-to-noise ratio of your average ERP waveforms. On the other hand, several factors favor a slower rate of stimulus presentation. First, sensory components tend to get smaller as the SOA and ISI decrease, and this reduction in signal might outweigh the reduction in noise that you would get by averaging more trials together. Second, if the subject is required to make a response on each trial, it becomes tiring to do the task if the interval between successive trials is very short. Third, a short SOA will tend to increase the amount of overlapping ERP activity (which may or may not be a problem, as described earlier). However, using a very long interval between stimuli to minimize overlap may lead to a different problem; namely, anticipatory brain activity prior to stimulus onset (especially if stimulus onset time is relatively predictable). My typical approach is to use an SOA of 1500 ms for experiments in which each trial consists of a single stimulus presentation and the subject must respond on each trial (e.g., an oddball experiment). I typically reduce this to 1000 ms if the subject responds on only a small proportion of trials, and I might increase it by a few hundred milliseconds for more difficult tasks or for groups of subjects who respond slowly. Of course, there are times when the conceptual goals of the experiment require a different set of timing parameters, but I find that this kind of timing is optimal for most relatively simple ERP experiments.
> 

### ***Stimuli***

*Stimuli Habituation*

“Given that a particular stimulus elicits a response, repeated applications of the stimulus result in decreased response (habituation). The decrease is usually a negative exponential function of the number of stimulus presentations … Other things being equal, the more rapid the frequency of stimulation, the more rapid and/or more pronounced is habituation … The effect occurs in terms of real time course and occurs within certain limits in terms of number of trials as well. [However,] if the stimulus is withheld, the response tends to recover over time (spontaneous recovery).”$^{7}$ Allowing for participant breaks and a longer ITI can allow for this response recovery, though the exact timing will require more precise literature review depending on project type.

If you are attempting to elicit strong emotional responses to a stimulus (fear, anger, etc.), be forewarned that responses are quick to habituate, particularly in a controlled experiment (Luck) and it may be difficult to collect enough data across a participant as their initial reaction diminishes due to repeat exposure.

*Sensory Confounds*

Hillyard principle: “responses should be compared to the same physical stimuli while holding overall arousal level and task demands constant, such that all that differs is the focus of selective attention.”$^{8}$ Rephrased: “To avoid sensory confounds, you must compare ERPs elicited by exactly the same physical stimuli, varying only the psychological conditions.” (Luck, 2014, pg. 134)

> Imagine an experiment in which “the target is the letter X, and the nontarget is the letter O. X is presented on 20% of trials, and O is presented on the other 80%.” As “the target and nontarget stimuli differ in terms of both shape and probability,”) this experiment is in violation of the Hillyard Principle. You could counterbalance the X’s and O’s (X is the target half the time, and O is the target the other half), though “*stimulus-specific adaptation”* remains*.* “Specifically, a difference in the probability of occurrence between two stimuli creates differences in sensory adaptation, which will in turn create differences in the sensory response to the two stimuli. The basic idea is that when the visual system encounters a particular stimulus many times, the neurons that code that stimulus will produce smaller and smaller responses. This is known as stimulus-specific adaptation or refractoriness .” “Instead of using X and O as the stimuli, we could use the letters A, B, C, D, and E. Each of these letters would occur on 20% of trials. We would then have five different trial blocks, with a different letter designated as the target in each block (e.g., in one block, we would say that D is the target and all of the other letters were nontargets). We could then present exactly the same sequence of stimuli in each trial block, with the target category (e.g., D) occurring on 20% of trials and the nontarget category (e.g., A, B, C, and E) occurring on the remaining 80%. This would solve the sensory adaptation problem, because the probability of any given physical stimulus is 20%, whether it is the target stimulus or a nontarget stimulus” (Luck, 2014, pg. 131-134).
> 

*Note:* In this specific experiment, we would vary the order of the letters within trials! Just because we keep the stimuli presentation the same does not mean the ordering must remain fixed. If anything, participants learning, implicitly or explicitly, aspects of the design when there is some element of “surprise” (and it is not the express purpose of the experiment for them to do so) can lead to inconsistent results.

*General Note*: “Large changes in brightness” from a monitor can “lead to event locked spikes in noise.”$^{9}$. In general, keep the recording setup and environment as consistent as possible across all trials and participants.

*Creation of Stimuli*

PsychoPy is a fantastic resource for stimuli creation; use this [resource](https://www.notion.so/10c8a22f142780f7963ec3d741dd2a10?pvs=21) for an indepth explanation and setup help.

### ***Data analysis***

Though this section of the wiki is dedicated to experimental design, with more in depth coverage of data processing to come, it would be remiss to exclude a brief discussion on data analysis now. It is a dangerous game to work on various stages of the project pipeline in isolation from one another: disregarding additional research once data collection has begun, ignoring a review of the data until all participants have been recorded. Instead, it is better practice to complete some preprocessing or rudimentary analysis after you have collected data from a participant or two. Ensure that the board has been set up with the pins in their correct placement, the proper channels in their right place. Ensure there is no obvious noise artifact in the recording environment that may be removed before the next collection period. If you need to make tweaks, it’s better to do so before you have fully invested time in recording data from a large group of participants, or invested several hours into a setup that, after a quick scan of the data, would prove unusable.

Remember: “data that are consistently noisy or have systematic artifacts are not likely to be much improved by artifact rejection” (-Jon Hansen of Hansen’s axiom)

### Even More Tips

The following is taken directly from Luck, 2014, page 144**.** Though they include specific tips referencing ERP experiments, they may still be broadly applicable across all project types. Despite a difference in evaluating particular components, the fundamentals of experimental design remain.

> ***Tip 1*** Whenever possible, avoid physical stimulus confounds by using the same physical stimuli across different psychological conditions (i.e., follow the Hillyard principle). This includes “context” confounds, such as differences in sequential order. Difference waves can sometimes be used to subtract away the sensory response, making it possible to compare conditions with physically different stimuli.
> 

> ***Tip 2*** When physical stimulus confounds cannot be avoided, conduct control experiments to assess their plausibility. Don’t assume that a small physical stimulus difference cannot explain an ERP effect, especially when the latency of the effect is less than 300 ms.
> 

> ***Tip 3*** Although it is often valid to compare averaged ERPs that are based on different numbers of trials, be careful in such situations and avoid using peak-based measures.
> 

> ***Tip 4*** Avoid comparing conditions that differ in the presence or timing of motor responses. This can be achieved by requiring responses for all trial types or by comparing subsets of trials with equivalent responses.
> 

> ***Tip 5*** To prevent confounds related to differences in arousal and preparatory activity, experimental conditions should be varied within trial blocks rather than between trial blocks. When conditions must be varied between blocks, arousal confounds can be prevented by equating task difficulty across conditions.
> 

> ***Tip 6*** Think carefully about stimulus timing so that you don’t contaminate your data with offset responses or overlapping activity from the previous trial.
> 
