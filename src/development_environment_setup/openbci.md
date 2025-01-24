By Priyal Patel for _Neurotech@Davis_

# What is OpenBCI?

OpenBCI is a neurotech company whose hardware we use to collect brain data. Using their GUI, we are able to visualize the data in real-time and access these recordings in "./Documents/OpenBCI_GUI".

# Installing GUI

Follow this [guide](https://openbci.com/downloads) to install the OpenBCI GUI.

Once the package appears in your “Downloads” folder, double click to open and keep clicking next button to fully install the package.

# How to Use

**Opening the GUI**

In Finder/File Explorer, look for "OpenBCI_GUI" in Applications and then double click on the app.

If the error message below pop-ups, then right click on the app and click "open".

**Starting a Secession**

First, you need to have the USB dongle plugged into the device running the GUI and the cyton board turned on with batteries. See 'Data Collection Steps & Help' in Additional Resources for more information.

Then, select these options:

- CYTON (live)
- Serial (from Dongle)
- 8 CHANNELS
- OpenBCI
- File

Under "Secession Data" you can add a custom secession name.

Finally, click either "START SECESSION" or "AUTO-CONNECT".

**Troubleshooting Errors**

There are many reasons for why a red error message will appear when trying to start a secession.

Here are some ways to fix these errors:

-Try clicking either "START SECESSION" or "AUTO-CONNECT" at least 5 times. It usually takes a couple seconds before the connection is established.

-Check that the batteries have been plugged into the cyton board and are facing the correct direction in the holder.

-Check there is a light on the cyton board and the switch is set to "PC".

-Check that there is a red light flashing on USB dongle. If not, then switch the black reset switch to the right and then back to the left.

-Relaunch the GUI and repeat the secession starting process.

-Replace any dead batteries.

-Use another device as the GUI runs better on some devices compared to others.

**Starting/Stopping a Stream**

Press "Start Data Stream" button to begin recording brain data. After, press "Stop Data Stream" button to stop recording data.

See 'GUI Widgets' in Additional Resources to learn more about other GUI features.

**Access Data**

In Finder/File Explore, under Documents open the "OpenBCI_GUI" folder. In "Recordings", find the secession folder by the custom name you provided or by the date/time the secession was started. Inside the secession folder find all recordings based on date/time the recording was started.

# Additional Resources

- [Data Collection Steps & Help](https://www.notion.so/dhruvsangamwar/Data-Collection-Steps-Help-aa6f47acb4be4ee894257f751f9f2efd?pvs=4)
- [GUI Widgets](https://docs.openbci.com/Software/OpenBCISoftware/GUIWidgets/)
