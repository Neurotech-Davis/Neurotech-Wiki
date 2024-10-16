# Filtering

Let us now discuss filtering. Before we discuss filtering, let’s make sure we understand well exactly what is going on when we look at a waveform in our program.

A filter suppresses or passes frequencies, which can be used to remove noise and isolate certain frequencies. A filter can be represented as follows:

![filtering](https://i.postimg.cc/0Nv5R4dg/Screenshot-2024-09-19-at-5-13-17-PM-1.png)

This is called the frequency response function of the filter. This function shows exactly what how much of the frequency it will let pass from the waveform. For example, when we convert our waveform to the frequency domain, the frequency 30Hz will get halved, and the frequency 80Hz will get removed, ie filtered out. 

Now that we know what a filter is, let’s talk about some different types of filters and how to use them. 

Low-pass filter: A low pass filter, or a high block filter, is a filter that allows frequencies lower than the specified frequency to pass and blocks any filters higher than the number.

High-pass filter: A high pass filter, or a low block filter, is a filter that allows frequencies higher than the specified frequency to pass and blocks any filter lower than the number.

Notch filter: Removes one frequency and passes the rest.

Band-pass filter: Combination of low pass and high pass. You can define the low end and high end of which frequencies you want to pass or keep.

## When should you filter?

In general, it is a good idea to filter between 0.1-30Hz. The 0.1Hz helps fix the drifts as discussed earlier in our experiment, and the 30Hz can help counteract muscle movements and line noise, however should change this based on your experiment. Here are some more special cases to help you select a filter:

1. If you are looking at slow or late components, you can consider using 0.1Hz or 0.05Hz
2. If you are looking at responses which happen under 50ms such as the auditory brainstem response, you should use higher cutoff frequencies for both low-pass and high-pass filters. You should do some research before selecting them.