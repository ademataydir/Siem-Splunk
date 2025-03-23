# SPLUNK INSTALLATION AND SETTINGS

## How to Install Splunk Enterprise & Splunk Universal Forwarder on Windows:
You can sign up for the www.splunk.com site and download and install the Splunk Enterprise app.

### Splunk Enterprise Installation steps;
We run the downloaded Setup file.

![image](https://github.com/user-attachments/assets/ebd6ea4e-a60e-4765-884f-bb61ea292e6b) 

On the first screen that comes up when the installation starts,  we must click on the box at the top and accept the license agreement. Otherwise, we will not be able to continue the installation process. When you click the box, the "Customize Options" and "Next" buttons at the bottom will be active. If we want to change and customize some installation settings, we press the "Customize Options" button. If we want to install it without making any setting changes, we press the "Next" button and proceed. After pressing the Next button, we go directly to the loading screen. Now, let's click the "Customize Options" button and see the settings there.

![image](https://github.com/user-attachments/assets/f1356fb5-1392-44b8-bbb9-92cde88db8a9) 

Here, it asks in which location we want to install the program. By default, it specifies that it will be installed in C:\Program Files\Splunk\. If we want to change it, we can change the location by pressing the "Change" button. Afterwards, we proceed by pressing the "Next" button.

![image](https://github.com/user-attachments/assets/a0826ef1-992e-4e16-a6e7-99a14eebd741) 

If Splunk will only run on a single server and only needs to access resources on the local system, the "Local System" account can be used. If Splunk needs to retrieve data from multiple servers or remote systems, a domain account can be used. This is suitable for installations that require access to other devices on the network. Here we will click on the "Local System" option and proceed.

![image](https://github.com/user-attachments/assets/7cdd0360-6141-402f-9691-439583dfdd1a) 

Here he wants us  to set a username and password for ourselves. We should write down this information as we may be asked to make any adjustments to Splunk Enterprise in the future.

![image](https://github.com/user-attachments/assets/f6aa4247-1639-4788-afd1-f909c95f66b7) 

Then we press the "Next" button again and proceed.

![image](https://github.com/user-attachments/assets/809b6b06-e5bd-40f8-948c-06446bab2dd1) 

After the installation is finished, we need to click on this box to create a shortcut to the Start menu in order to run Splunk whenever we want. Then we press the "Install" button and start the installation. When the installation is finished, a screen with a "Finish" button at the bottom will appear. When you click the Finish button, our Splunk Enterprise installation is completed

### - Now we need to install Splunk Universal Forwarder on our devices  in order to receive logs from our devices to Splunk Enterprise.

www.splunk.com is a member of the site and the Splunk Universal Forwarder application is downloaded and installed.
# Splunk Universal Forwarder installation steps;
We run the Setup file that we downloaded.

![image](https://github.com/user-attachments/assets/ca26cc77-9e46-4c9f-9f18-39774a11fdfe) 

On the first screen that comes up when the installation starts,  we must click on the box at the top and accept the license agreement. Otherwise, we will not be able to continue the installation process. When you click the box, the "Customize Options" and "Next" buttons at the bottom will be active. If we want to change and customize some installation settings, we press the "Customize Options" button. If we want to install it without making any setting changes, we press the "Next" button and proceed. After pressing the Next button, we go directly to the loading screen. Now, let's click the "Customize Options" button and see the settings there.

![image](https://github.com/user-attachments/assets/da920fa2-6a79-4ecb-8655-ed497d43a678)

Here, it asks in which location we want to install the program. By default, it specifies that it will be installed in C:\Program Files\SplunkUniversalForwarder\. If we want to change it, we can change the location by pressing the "Change" button. Afterwards, we proceed by pressing the "Next" button.

![image](https://github.com/user-attachments/assets/bc840d3f-c51c-4c91-8775-8f7a44cebfde)

Here, if we have a certificate of our own that we want to identify, we define it. When installing Splunk Universal Forwarder, the certificate identification section is used to ensure that data is transmitted securely encrypted. These certificates typically help secure data transmission between the Splunk forwarder and the Splunk indexer. The purpose of the certificates is to ensure the protection of data using the TLS (Transport Layer Security) encryption protocol. This is especially crucial in situations where sensitive data needs to be transmitted. The transmitted data is encrypted, the integrity of the data is maintained, and the identities of both parties in communication are verified. This security measure is especially important when transmitting data on open networks. If you are working in a small environment, you can use self-signed certificates, but for larger, corporate and secure environments, a CA-signed certificate is more appropriate. We proceed by pressing the "Next" button.

![image](https://github.com/user-attachments/assets/bd0d3ee8-6fb0-4ae9-8cdc-dc23be9800ab)

- If you are building an installation that will only work on the local system and does not require network access, "Local System" may be sufficient.

- If you are going to work on the network and need access to domain resources, it would be more appropriate to choose "Domain Account".

- "Virtual Account", on the other hand, is used according to security and isolated transaction requirements.

- Here, we select the "Local System" option and say "Next" and proceed.

![image](https://github.com/user-attachments/assets/86a08239-4a13-41b4-a394-3b7d351d8d40)

Here, we click on the relevant boxes to determine which Logs we want  Splunk Universal Forwarder to send to Splunk Enterprise from the device on which it is installed, and then click the "Next" button to proceed.

![image](https://github.com/user-attachments/assets/886efece-265f-43cb-b0cb-1f4a020b1da3)

### What is Deployment Server?
Deployment Server provides centralized configuration and application deployment to Universal Forwarders (and other Splunk components) in the Splunk environment. This means that Deployment Server works as a "central configuration server", which allows you to manage each forwarder in batches without having to configure it manually. The Deployment Server stores certain configuration files (for example, inputs.conf, outputs.conf, props.conf, etc.). Automatically forwards to Splunk Universal Forwarders. Different configurations can be distributed to forwarders. For example, different log collection and forwarding settings can be made for different groups of forwarders. When any changes are made, this change is automatically applied to all destination forwarders.
### When to Choose the "Deployment Server" Option
If you plan to centrally manage many Universal Forwarders and want to automatically distribute configuration files to each forwarder, enabling Deployment Server may be a good option. If you are only installing a single Splunk Forwarder and do not need centralized management, you do not need to choose the Deployment Server option. Deployment Server is used to centrally manage multiple Forwarders in a Splunk environment and deploy their configurations. We proceed by pressing the "Next" button.

![image](https://github.com/user-attachments/assets/841a9327-255d-4961-ab05-1d4cb0dd9427)

This option determines where the Universal Forwarder sends the log data it collects. The terms "Receiver" and "Indexer" refer to the components of Splunk through which data is processed and stored.
### What are Receiver and Indexer?

### Receiver
The Splunk Receiver is the point where the data is received. This is usually Indexer in Splunk Enterprise or Splunk Cloud. The receiver receives the data streams and sends this data for later indexing (processing). That is, Forwarders send data to the Receiver.

### Indexer
Indexer is the component where Splunk processes and indexes data. This is the component where the data becomes searchable and the Splunk search engine works. Indexer takes the data, processes it, and then stores the data in a searchable format.

### When to Use the Receiver Indexer Option
Receiver Indexer specifies the Splunk instance from which your Forwarder will receive the data. That is, the Forwarder is configured to send data to a Receiver or Indexer.
When you select this option, Forwarder: It will forward the data it collects to a specific Receiver or Indexer. If you have a central Splunk Enterprise Indexer, data will be sent to this Indexer.

### Summarize
The Receiver Indexer is used to determine where the Universal Forwarder will send the data. This allows data to be transmitted to a central Splunk Indexer. This indexer then indexes the data and makes it searchable. If the data needs to be sent to an Indexer in Splunk Enterprise or Splunk Cloud, you will need to select this option. Here we write the IP number and port 9997 of our Splunk Enterprise. Logs will be sent to this port. That's why Splunk Enterprise's port 9997 must be open. I will explain how to open this port later. . We proceed by pressing the "Next" button.

![image](https://github.com/user-attachments/assets/9837b66c-d9d0-442d-81c2-a21fdd2966c5)

Now we press the "Install" button and start the installation. 

![image](https://github.com/user-attachments/assets/05f5ccd5-0f00-462d-a009-758b5b1cd3ac)

When  the installation is finished, a screen with a "Finish" button will appear. When you click the Finish button, our Splunk Universal Forwarder installation is completed.

![image](https://github.com/user-attachments/assets/3aa8712f-40ae-44a0-a58f-bd6c0375107c)

In order for Splunk Universal Forwarder to work, we must right-click on Splunk Forwarder in the Services section in the Task Manager and do Restart.

### - Now we need to make some adjustments in Splunk Enterprise so that logs can be transmitted from Splunk Universal Forwarder to Splunk Enterprise.
