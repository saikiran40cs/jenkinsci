# Jenkins {#jenkins}

### Install Jenkins {#install-jenkins}

1. Download the latest Jenkins war file  [here](http://mirrors.jenkins-ci.org/war/latest/jenkins.war).

### Run and Configure Jenkins {#install-jenkins}

1. Run Jenkins with the command`java -jar jenkins.war`. To change the default port of the web interface of Jenkins, use the argument`--httpPort=$port`.  


   For example,`java -jar jenkins.war --httpPort=12345`

2. Open url`http://server:port`in browser to configure Jenkins. In the last example, it is`http://localhost:12345`.

3. Download and install plugins following the steps below.

   1. 2. 3. Switch to the`available`tag and search for the plugin. In this example, the`Github Project`plugin is installed to integrate Jenkins with projects on github.



      Click on the`install`button

   4. After the installation is finished, you can configure jobs to use existing Github projects.

### Create Jobs {#create-jobs}

In this simple example, a job is created to compile a c program and run it.

1. Create a Job at
2. Choose free-style project and name it.

3. The following setting page should show. Ignore most of them for now and go to the`build`section.

4. Choose`execute shell`.

5. Enter simple shell commands that compile and run a hello world c program.

6. Click`save`and the job should appear in the dashboard.

7. Click on the job and go to the configuration page.

   Click and the project will be built with the preconfigured build-steps.

   A new successfully built record should appear in the project's build history.

### References {#references}

[Jenkins Website](https://jenkins-ci.org/)

[Install Jenkins](https://wiki.jenkins-ci.org/display/JENKINS/Installing+Jenkins)

[Start and Configure Jenkins](https://wiki.jenkins-ci.org/display/JENKINS/Starting+and+Accessing+Jenkins)

