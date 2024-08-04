By Priyal Patel for _Neurotech@Davis_

**What connects all the topics we have covered so far together?**

the BCI Pipeline 🎉

**What is a BCI?**

A brain computer interface, which means some kind of project that incorporates brain signals in performing a task or predicting a result.

**What is a Pipeline?**

A way to represent how different components of your project are "connected" together.

**How would you link components of a project together?**

Using connectors, the special glue. Some modern day examples include bluetooth, usb, electrode gel, python libraries, node-red toolbox, and so many more.

When researching connectors, two key questions to Google: 

1. How can [component x] communicate or link with [component y]?
   - see how other people have tried to link these components
2. What are the limitations of using [connector z]?
   - see what problems people have had using this type of connector & their suggestions for alternative connectors

Usually there won't be a direct mention of a "BCI pipeline" in a research paper or open-source project; however, by the identifying the steps below in these online sources, you can gain ideas for how people went about forming their pipelines.

**Keys Steps in our BCI Pipeline**

<img width="527" alt="BCI Pipeline" src="https://github.com/user-attachments/assets/1a09c30e-b14d-43ce-8ad6-f4aaf7c40b13">


1. Electrodes are placed on the scalp with electrode gel
2. The brain produces electrical signals that are picked up from the scalp by the electrodes
3. The analog signals from the EEG (electroencephalogram) electrodes are converted to digital signals by the signal processing hardware
4. The digital signals are passed to the laptop hardware UI program using bluetooth communication from signal processing hardware to usb
5. These digital signals are displayed by the hardware's UI program revealing wave like patterns
6. The amplitude (height of the waveform) is measured in microvolts and is read per second by the preprocessing program running
7. The preprocessing program applies filters to remove uncharacteristic microvolt values and any additional changes to the data occur in this step
8. The cleaned data is passed as input to the algorithm or machine learning model to perform a task or predict an outcome
9. Finally, the output from the algorithm or machine learning model is printed to display on the laptop "Person is focused"
10. This happens in real-time: each step can be occurring simulataneously as electrical signals are constantly being collected from the scalp
