## Instant Analysis with SonarQube {#during-analysis}

---

**Pre-requisite is to configure SonarQube with Jenkins**

_**Step 4:**_**Job Configuration**

1. **Configure** the project, and scroll down to the **Build** section.
2. Add the _Execute the SonarQube Scanner \_build step to your build_.\_
3. Configure the SonarQube analysis properties. You can either point to an existing _**sonar-project.properties**_ file or set the analysis properties directly in the **Analysis properties ** field.

![](/assets/sonarqube_job_config.png)

Now build the job to get the tests analysed and run the tests instantly.

This is the beginning for learning to analyse the code...

