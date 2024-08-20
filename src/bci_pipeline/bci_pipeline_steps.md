By Priyal Patel for _Neurotech@Davis_

**Keys Steps in our BCI Pipeline**

<img width="498" alt="BCI Pipeline" src="https://github.com/user-attachments/assets/f0de2efd-7f5c-460f-a6b5-9eaceac6b641">

1. EEG (electroencephalogram) electrodes are placed on the scalp with electrode gel
2. The brain produces continuous electrical signals (analog signals) that are picked up from the scalp by the electrodes
3. These analog signals collected from the electrodes are converted to digital signals (non-continuous & discrete values) by the signal processing hardware
4. Using bluetooth communication between the signal processing hardware and a bluetooth usb, the digital signals are passed to the hardware's UI program running
5. These digital signals are displayed in by the hardware's UI program revealing wave like patterns
6. The amplitude (height of the wave) of each wave measured in microvolts is collected per second and passed as input to the preprocessing program running
7. The preprocessing program applies filters to remove uncharacteristic microvolt values and any additional necessary changes to the data occur in this step
8. The cleaned data is passed as input to the algorithm or machine learning model to perform a task or predict an outcome
9. Finally, the output from the algorithm or machine learning model is printed to display on the laptop "Person is focused"
10. This happens in real-time: each step can be occurring simulataneously as electrical signals are constantly being collected from the scalp
