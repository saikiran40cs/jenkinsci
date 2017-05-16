## SCTM Result Analysis with Jenkins {#during-analysis}

---

> _**Pre-requisite is to configure **_[_**SonarQube with Jenkins**_](https://nsaikiran.gitbooks.io/jenkins/content/Jenkins Configurations/22-configure-sonarqube-with-jenkins.html)

### **Job Configuration**

1. Click on the "New Job" link and enter a Job name. Select the "Build a free-style software project" radio button and click OK.

   ![](/assets/SCTM_1.jpg)

   1. Configure your Job settings as required. To add a SCTM build step, scroll down to the "Build" section and select "SilkCentral Test Manager Execution" from the "Add Build step" drop down.

   ![](/assets/SCTM_2.jpg)

   1. Enter the SCTM Execution Plan ID you wish to execute and also the SCTM Project ID that contains this execution plan.

   ![](/assets/SCTM_3.jpg)

   1. Click the "Advanced" button to configure other options when running the SCTM execution plan such as continue on error, collect results, build numbers to be used. Click "Save" to save the job.

   ![](/assets/SCTM_4.jpg)

   1. Once save click on the Workspace link for the job you just created.

   ![](/assets/SCTM_5.jpg)

   1. You will receive an error stating that the project does not have any Workspaces, this is because no builds have been performed yet. To do this click on the "Run a build" link.

   ![](/assets/SCTM_6.jpg)

   1. This will start the SCTM execution and you can see the pending status on the Jenkins project page.

   2. Once the execution has started you will get an 'in progress' icon. Click on the build number to view the progress of the job under execution

      ```
      Console Output

      14:38:47 Started by user Sai Kiran Nataraja
      14:38:47 Building on master in workspace D:\Jenkins\workspace\SaiTest
      14:38:47 No emails were triggered.
      14:38:48 INFO: Login on Silk Central.
      14:38:48 INFO: Start execution plan 'Configuration_Suite' (1,199).
      14:38:48 INFO: Waiting for result of execution plan 'Configuration_Suite' (1,201).
      15:29:05 INFO: Received result for execution plan 'Configuration_Suite' (1,201).
      15:29:07 Build step 'Collect Silk Central Test Results' changed build result to STABLE
      15:29:07 [BFA] Scanning build for known causes...
      15:29:07 [BFA] No failure causes found
      15:29:07 [BFA] Done. 0s
      15:29:07 No emails were triggered.
      15:29:07 Finished: STABLE
      ```

   3. Once the execution has completed you will see the screen below.

   ![](/assets/SCTM_8.jpg)

   1. If you then go to the Execution Plan in SCTM you will see that it was executed and the build information has been brought over from Jenkins.

   ![](/assets/SCTM_9.jpg)



**Note:**In this case the build was "1", you can define which build number is used in the Advanced settings for the SCTM build step, see point 4 above.

Now if you run a new build in Jenkins for this job the SCTM execution will automatically be executed.



