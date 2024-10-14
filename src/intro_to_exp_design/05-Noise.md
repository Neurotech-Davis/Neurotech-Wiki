# Sources of Noise + Ways to Minimize Them
By Sofia Fischel for Neurotech@Davis

*Read more about artifacts [here](https://www.learningeeg.com/artifacts) (includes practice and an atlas reference showing specific EEG recordings)*

Much of the noise in EEG signals comes from “other biological signals such as skin potentials and from other non biological electrical noise sources in the environment” (Luck, 2014, pg. 149)

### **Source: Electrical devices** in the recording environment.

**Explanation**: “The flow of current through a conductor is always accompanied by a magnetic field that flows around the conductor. Moreover, if a magnetic field passes through a conductor, it induces an electrical current. These two principles are illustrated in figure 2.1, which shows what happens when a current is passed through one of two nearby conductors. The flow of current through one of the conductors generates a magnetic field, which in turn induces current flow in the other conductor. This is how electrical noise in the environment (e.g., the 120 V in the video display) can induce electrical activity in an ERP subject, in the electrodes, or in the wires leading from the electrodes to the amplifier”. Additionally, electrical noise is present from electronic devices in the recording environment: phones, computers, etc., as well as power lines.” (Luck, 2014, pg. 38)

![Figure 1](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfH4q9gGaAP2tubRUj2i9FqJbWKE1Xut4DeMau_e9SIbFyiR2J3tdqy1kB_QJyD7M2qsbQ1Q0oWgeMdzfpe7OoZTbcbVlCR4yvwJChn-XLXX6pEVoI4fpgmubH80gjOkrw9Gum-H6GSvxQkf8QlDm7bWrQ_?key=Bz0jFeL15qvzNHkoGa5FlQ)

Figure 1, source: Luck, 2014

**Solution:** Though it is impossible to remove all environmental noise, placing nearby devices on airplane mode may reduce some. Further, applying a notch filter (at 60 Hz) to remove ambient electrical current that may remain from additional sources occurs during preprocessing.

### **Source: Biological signals** from the participant

**Source: Blinks**

Explanation: “Within each eye, there is a large, constant electrical potential between the cornea at the front of the eye and the retina at the back of the eye (the corneal-retinal potential), which is like a dipole with positive at the front of the eye and negative at the back of the eye. This potential spreads to the surrounding parts of the head, falling off gradually toward the back of the head.” (Luck, 2014, pg. 194) “When the eyes blind, the eyelid moves across the eyes, which acts as a variable resistor that changes the EOG voltage recorded from electrodes near the eyes”. 

Additional explanation: [blink](https://www.learningeeg.com/artifacts#eye-blinks)

**Solution:** One possibility is to ask participants not to blink during critical periods of the task and then provide cues for periods when they can blink freely.” However, “[a]s both blinking and spontaneous eye movement are automatic behaviors, withholding either of them requires voluntary attention that might interact with task performance as well as introduce EEG signal.” In fact, instructing participants to not blink may contribute to a lessened response: “Ochoa and Polich directly tested the possibility of dual-task interference by giving subjects an oddball task and either telling them to avoid blinking or saying nothing at all about blinking. The P3 had a smaller amplitude and a longer latency when subjects were asked to avoid blinking.” (Luck, 2014, pg. 211). In practice, spotting a blink within the raw EEG signal is not difficult; while recording, you can remind participants to limit blinks — to the best of their ability — though they may just be an artifact removed during preprocessing. 

**Source**: **Eye Movements**

Explanation: “Eye movements are a result of the strong dipole inside the eye. When the eyes are stationary, this dipole creates a static voltage gradient across the scalp, which is removed by baseline correction and high-pass filters. When the eyes move, the voltages becomes more positive over the side of the head that they eyes now point toward “ (Luck, 2014, pg. 198)

Additional explanation: [lateral eye movements](https://www.learningeeg.com/artifacts#lateral-eye-movements)

**Solution:** If eye movements are believed to contaminate your data, using a central fixation point (and instructing participants to keep their vision focused upon it) is one solution. Further, the characteristic shape of “real eye movevements” (a “boxcar-shaped voltage deflection” resulting from “subjects mak[ing] a saccade from the fixation point to some other location and then … another saccade to return to the fixation point”) helps in making it distinct from noise, improving pre-processing ease (Luck, 2014, pg. 198-9). 

**Source: EMG signals**

Explanation: “The temporalis muscles are powerful muscles that we use to contract our jaws, and they are located right under the T7 and T8 electrodes [see figure 2 below]. If you see a lot of EMG in this region of the head, you can ask the subject to relax his or her jaw and avoid teeth-clenching. The temporalis muscles are so large, however, that you will see small but consistent highfrequency EMG artifact at T7 and T8 throughout the session in some subjects, even when they try to relax.” (Luck, 2014, pg. 205)

“The muscles of the neck are the remaining common source of EMG noise. If a mastoid reference is used, this activity may be picked up by the reference electrode and therefore appears in all channels that use this reference. If a different reference site is used, EMG noise arising from the neck appears at the most inferior occipital and temporal electrode sites. It can usually be minimized by asking the subject to sit straight upright rather than leaning the head forward. Neck EMG can also be minimized by having the subject sit back in a recliner with the head leaning against the recliner, but this can cause artifacts in the occipital electrodes.” (Luck, 2014, pg. 206)

Additionally, “It turns out that there is a strong electrical gradient between the base of the tongue and the tip of the tongue. Consequently, when the tongue moves up and down in the mouth, it creates large voltages that propagate to the surface of the head. These voltages are called glossokinetic artifacts” (Luck, 2014, pg. 207)

Additional explanation: [chewing and hypoglossal movement](https://www.learningeeg.com/artifacts#chewing), [muscle](https://www.learningeeg.com/artifacts#myogenic)

**Solution:** Instruct participants to remain as still as possible, reacting only in ways that align with their specific task response. Additionally, try to avoid trials that necessitate head movements, verbal responses, or any sort of movement beyond a stationary position. “[Neck muscles] can usually be minimized by asking the subject to sit straight upright rather than leaning the head forward. [They] can also be minimized by having the subject sit back in a recliner with the head leaning against the recliner, but this can cause artifacts in the occipital electrodes” (Luck, 2014, pg. 206). “When such [movement] tasks can not be avoided, one should try to plan the experiment so that the periods of movement do not overlap with critical periods of data collection.”$^{9}$ Of course, if your project necessitates movement of some kind (e.g., looking between different screens, etc.) attempt to limit it as much as is feasible (i.e. eye movement instead of head movement). Otherwise, if the project truly necessitates a large movement, plan accordingly for the applicable noise.

**IMPORTANT TIP:** Incidental movements are almost a given. Record timestamps of these movements, as this will better facilitate the preprocessing phase if you are able to quickly locate EMG signals.

### **Source: Fatigue**

Explanation: Participants may grow fatigued from a long trial length or repeat exposure to repeat stimuli. This can be an issue two-fold: their response to the stimulus may decrease as their mind wanders and they grow fidgety and restless, increasing noise.

**Solution**: Keep recording sessions on the shorter side. Additionally, it is recommended to give participants breaks in between trials.

### **Source: Electrode or Cable movement**

Explanation: “Cable sway in non-wireless systems … causes artifacts. This can be attributed to the motion of the conductor within the magnetic field or to triboelectric noise that is caused by friction of the cable’s components.”$^{5}$

“a movement in the electrodes will sometimes cause the voltage to change suddenly to a new level” (Luck, 2014, page 202)

**Solution:** Minimize movement of the EEG setup as much as possible. Ensure that wires do not cross over one another during recordings. Much like EMG signals, cable sway can be minimized by keep participants as stationary as possible within the confines of the experimental procedure.

### **Source: Poor ground connection or reference interference**

Explanation: “a poor ground connection … should be the first thing checked whenever trouble shooting noise problems. ... Common causes of a floating ground can be a broken ground wire, the wire coming loose from the grounding site …, using a ground site too far from the recording, a broken wire/pin on the electrode or headstage, or a malfunctioning headstage.”$^{6}$

Note: “You can never record the voltage at a single scalp electrode. Rather, the EEG is always recorded as a potential for current to pass through one electrode (called the active electrode) to some other specific place. This “other specific place” is usually a ground electrode” (Luck, 2014, pg. 150)

**Solution**: Check the recording equipment for any noticeable issues.

### **Source: Reference interference**

Explanation: “Avoid using a reference that introduces a lot of noise into your data (a reference electrode near the temporalis muscle will pick up a lot of muscle-related activity… [which] will then be present in all channels that use this reference”. Additionally, “any noise in the reference electrode will be present in all electrodes that use this reference ... Thus, if you see some noise in all the channels that share a particular reference site, then the noise is almost certainly coming from the reference site.” (Luck, 2014, pg. 162)

**Solution**: In picking a reference, consult the literature to establish a conventional reference away from potential confounding noise.

### **Source: Overheating equipment**

**(*Not quite as prevalent, though still something to keep in mind!)***

Explanation: “In the unlikely event that you are able to eliminate all other sources of noise, your signal will still have thermal noise. This is caused by Brownian motion in conductors or semiconductors in the entire signal path before the signal is digitized (including the electrode itself), and since Brownian motion is independent in every location, it cannot be removed or reduced by a reference. Luckily though thermal noise is unlikely to drastically interfere with the electrophysiological signal as long as none of your devices are overheating.”

**Solution**: “Make sure that electronics are properly ventilated and kept in a cool environment.”$^{6}$ Additionally, recording in a cool place means that there is less sweat and skin potentials, so less noise overall!
