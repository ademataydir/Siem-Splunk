## How to Install Splunk Enterprise on Windows
You can sign up for the www.splunk.com site and download and install the Splunk Enterprise app.

### Splunk Enterprise Installation steps;
We run the downloaded Setup file.

![image](https://github.com/user-attachments/assets/e706ebac-84bb-4390-ba67-d5964bf1122f) © Splunk Inc.

On the first screen that comes up when the installation starts,  we must click on the box at the top and accept the license agreement. Otherwise, we will not be able to continue the installation process. When you click the box, the "Customize Options" and "Next" buttons at the bottom will be active. If we want to change and customize some installation settings, we press the "Customize Options" button. If we want to install it without making any setting changes, we press the "Next" button and proceed. After pressing the Next button, we go directly to the loading screen. Now, let's click the "Customize Options" button and see the settings there.

![image](https://github.com/user-attachments/assets/6c72edbd-c251-4e9f-a5ae-26ba94bcb27f) © Splunk Inc.

Here, it asks in which location we want to install the program. By default, it specifies that it will be installed in C:\Program Files\Splunk\. If we want to change it, we can change the location by pressing the "Change" button. Afterwards, we proceed by pressing the "Next" button.

![image](https://github.com/user-attachments/assets/23a6c1fe-5597-4e56-b8e0-625516df1a99) © Splunk Inc.

If Splunk will only run on a single server and only needs to access resources on the local system, the "Local System" account can be used. If Splunk needs to retrieve data from multiple servers or remote systems, a domain account can be used. This is suitable for installations that require access to other devices on the network. Here we will click on the "Local System" option and proceed.

![image](https://github.com/user-attachments/assets/06fc3858-01a7-4ded-bcfe-267b875c1262) © Splunk Inc.

Here he wants us  to set a username and password for ourselves. We should write down this information as we may be asked to make any adjustments to Splunk Enterprise in the future.

![image](https://github.com/user-attachments/assets/c5627a95-5423-43c0-8678-b2af7dc16ab8) © Splunk Inc.

Then we press the "Next" button again and proceed.

![image](https://github.com/user-attachments/assets/f5789977-b04d-4c17-b26b-198798200db2) © Splunk Inc.

After the installation is finished, we need to click on this box to create a shortcut to the Start menu in order to run Splunk whenever we want. Then we press the "Install" button and start the installation. When the installation is finished, a screen with a "Finish" button at the bottom will appear. When you click the Finish button, our Splunk Enterprise installation is completed.

### Now we need to make some adjustments in Splunk Enterprise so that logs can be transmitted from Splunk Universal Forwarder to Splunk Enterprise.

![image](https://github.com/user-attachments/assets/00aca8f6-7844-461e-8fee-b8fe8e890e60) © Splunk Inc.

On the Splunk Enterprise screen, we enter the "Forwarding and Receiving Indexes" section in the "Settings" section at the top right.

![image](https://github.com/user-attachments/assets/e5df2567-9097-456d-8def-13417977bcc9) © Splunk Inc.

Click on the "Configure receiving" button in the "Receive data" section on the screen that opens.

![image](https://github.com/user-attachments/assets/7dda47da-6657-4b66-9274-0d23bfa19553) © Splunk Inc.

On the page that opens, click on the "New Receiving Port" button in the upper right section.

![image](https://github.com/user-attachments/assets/741a8abe-caa9-4aea-983e-81a274f11378) © Splunk Inc.

When installing Splunk Universal Forwarder, we wrote the port number to which we will send the logs. That port must be open here in order for the logs from there to be retrieved from here. If it is not open, we must open it.  Since we write 9997  there, we write the same here and press the "Save" button.

![image](https://github.com/user-attachments/assets/9d39f07f-c599-4155-8b08-25f0cf70d7e1) 

© Splunk Inc.

The Port we added appears in the list. It should be enable so that the logs can come.

This is the page where we can open, close, add, delete ports to Splunk Enterprise.

### * Now we need to install Splunk Universal Forwarder on our devices  in order to receive logs from our devices to Splunk Enterprise.

- [Splunk Universal Forwarder installation steps on Windows](https://github.com/ademataydir/splunk-universal-forwarder-installation-steps-on-windows)
- [Splunk Universal Forwarder installation steps on Linux](https://github.com/ademataydir/splunk-universal-forwarder-installation-steps-on-linux)

### ** Now, to monitor our system more effectively, we need to create dashboards for several use cases based on the logs collected by Splunk Universal Forwarder and sent to Splunk Enterprise.

- [Splunk Use Cases & Dashboards](https://github.com/ademataydir/splunk-use-cases)

### Note
This content has been prepared for personal learning purposes related to the installation of Splunk software. All screenshots and software are the property of Splunk Inc. This page is not intended for commercial use.
