## Instant Analysis with SonarQube {#during-analysis}

---

_**Step1:**_**Set environment variables for SONAR\_RUNNER\_HOME**

Open your environment variables window. Click new button in System variables section.

1. Set a variable name SONAR\_RUNNER\_HOME and its value should be the unzipped path of sonar-runner zip file.

   Example:- variable name:- SONAR\_RUNNER\_HOME variable value:- C:\sonar-scanner

2. And then append sonar-runner's bin path %SONAR\_RUNNER\_HOME%\bin to the environment variables path.

   Example:- variable name:- PATH variable value:- %SONAR\_RUNNER\_HOME%\bin;

_**Step 2: **_**Install the **[**SonarQube Scanner**](https://plugins.jenkins.io/sonar)** for Jenkins via the Jenkins Update Center**

1. Configure your SonarQube server\(s\)
2. Log into Jenkins as an administrator and go to **Manage Jenkins &gt; Configure System**: Scroll down to the **SonarQube configuration** section, click on **Add SonarQube**, and add the values you're prompted for.

![](https://nsaikiran.gitbooks.io/sonarqube/content/assets/SonarQube_JenkinsIns.JPG)

Generate the user token by logging into the SonarQube website and provide the key details in Jenkins.

_**Step 3:**_**Configure the tools in Jenkins Global Configuration**

This step is mandatory if you want to trigger any of your SonarQube analyses with the SonarQube Scanner. You can define as many scanner instances as you wish. Then for each Jenkins job, you will be able to choose with which launcher to use to run the SonarQube analysis.

1. Log into Jenkins as an administrator and go to **Manage Jenkins &gt; Global Tool Configuration**
2. Scroll down to the **SonarQube Scanner** configuration section and click on **Add SonarQube Scanner**. It is based on the typical Jenkins tool auto-installation. You can either choose to point to an already installed version of SonarQube Scanner \(uncheck 'Install automatically'\) or tell Jenkins to grab the installer from a remote location \(check '_Install automatically_'\).
   ![](https://nsaikiran.gitbooks.io/sonarqube/content/assets/SonarQube_JenkinsToolConfiguration.JPG)

If you don't see a drop down list with all available SonarQube Scanner versions but instead see an empty text field then this is because Jenkins still hasn't downloaded the required update center file \(default period is 1 day\). You may force this refresh by clicking 'Check Now' button in **Manage Plugins &gt; Advanced tab**.

_**Step 4:**_**Job Configuration**

1. **Configure** the project, and scroll down to the **Build** section.
2. Add the _Execute the SonarQube Scanner \_build step to your build_.\_
3. Configure the SonarQube analysis properties. You can either point to an existing _**sonar-project.properties**_ file or set the analysis properties directly in the **Analysis properties ** field.

![](https://nsaikiran.gitbooks.io/sonarqube/content/assets/SonarQube_JenkinsInstantCodeReviewConfig_Jobs.JPG)

Now build the job to get the tests analysed and run the tests instantly.

This is the beginning for learning to analyse the code...

