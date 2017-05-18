## Configure SCTM with Jenkins {#during-analysis}

---

The first thing that needs to be done is to install the SCTM Executor plugin into Jenkins, to do this:

1. Open Jenkins in a browser

2. On the Welcome screen click on the "Manage Jenkins" link

3. Click on the "Manage Plugins" link

4. On the Plugin Manager screen click on the "Available" tab

5. Scroll down to find the "**SCTMExecutor**" plugin, check the box beside it and click the "**Download now and install after restart**" button

![](/assets/SCTM_Installation_1.jpg)

1. Once Jenkins has restarted, click on the "Installed" tab and you will see that the SCTMExecutor plugin is now installed. Then check the box beside the SCTMExecutor plugin to enable it

2. Click on the "Restart Once No Jobs Are Running" button

![](/assets/SCTM_Installation_2.jpg)

1. This completes the installation of the SCTM Executor plugin.

## Configure Jenkins in order to connect to your SCTM installation

Perform the below steps to connect to your SCTM installation

1. On the "Manage Jenkins" screen click on the "Configure System" link.

![](/assets/ManageJenkins.PNG)

2. Scroll down to the "_**SilkCentral TestManager Configuration**_" section and enter your SCTM installation details. Click on the "_**Test Connection**_" button to ensure you can connect to SCTM.

![](/assets/SCTM_ConfigurationSettings.PNG)3. This completes setting up the connection from Jenkins to SCTM.



