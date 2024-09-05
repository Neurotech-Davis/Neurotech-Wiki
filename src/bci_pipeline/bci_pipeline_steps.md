By Priyal Patel for _Neurotech@Davis_

**Keys Steps in our BCI Pipeline**

**Big Picture**

<img width="450" alt="bci_pipeline" src="https://github.com/user-attachments/assets/5e473367-c437-4a60-8481-8a784c220734">

**Steps**

1. EEG (electroencephalogram) electrodes are placed on the scalp with electrode gel

<img width="175" alt="brain" src="https://github.com/user-attachments/assets/8a7edc8e-9924-4d02-ab2c-f3a48bcf4918">

2. The brain produces continuous electrical signals (analog signals) that are picked up from the scalp by the electrodes

3. These analog signals collected from the electrodes are converted to digital signals (non-continuous & discrete values) by the signal processing hardware

![Signal Processing Hardware (1) 6 41 06 PM](https://github.com/user-attachments/assets/21560fcf-f858-4130-83fd-004b29ec5057)
![Signal Processing Hardware (2) 6 41 06 PM](https://github.com/user-attachments/assets/ae475146-384d-4a9a-826f-a9504bf5aae1)

4. Using bluetooth communication between the signal processing hardware and a bluetooth usb, the digital signals are passed to the hardware's UI program running

<p align="center"> <img width="250" alt="hardware" src="https://github.com/user-attachments/assets/6389092b-6abe-4b12-8ae6-fb55205d686c"/> </p>

![Signal Processing Hardware (6)](https://github.com/user-attachments/assets/69483fd9-e502-46c2-97a6-027a5d90a3ea)

6. These digital signals are displayed in by the hardware's UI program revealing wave like patterns

![Signal Processing Hardware (7)](https://github.com/user-attachments/assets/5ad9f2d4-3d49-449e-9ddd-5ab087c8f433)


7. The amplitude (height of the wave) of each wave measured in microvolts is collected per second and passed as input to the preprocessing program running

![Signal Processing Hardware (8)](https://github.com/user-attachments/assets/f5d9950e-5e3b-44e1-9738-f719c2521e22)

8. The preprocessing program applies filters to remove uncharacteristic microvolt values and any additional key changes to the data occur in this step

9. The cleaned data is passed as input to the algorithm or machine learning model to perform a task or predict an outcome

![Signal Processing Hardware (9)](https://github.com/user-attachments/assets/a112eea7-2cf1-436f-86ad-f1b726cc81c4)

10. Finally, the output from the algorithm or machine learning model is printed to display on the laptop: "Person is focused"

![Signal Processing Hardware (10)](https://github.com/user-attachments/assets/5cf07775-531e-476e-b08b-355b2a4de6b3)


11. This happens in real-time: each step can be occurring simulataneously as electrical signals are constantly being collected from the scalp
