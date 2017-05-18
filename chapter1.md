# Jenkins Basics {#jenkins-documentation}

---

Jenkins is a self-contained, open source automation server which can be used to automate all sorts of tasks such as building, testing, and deploying software. Jenkins can be installed through native system packages, Docker, or even run standalone by any machine with the Java Runtime Environment installed.

Currently there are two flavours of Jenkins.

1. [Jenkins - Open Source Version](https://jenkins.io/)
2. [CloudBees Jenkins Enterprise Edition](https://www.cloudbees.com/products/cloudbees-jenkins-enterprise)

Jenkins Pipeline\(One of the important feature\) is a suite of plugins which supports implementing and integrating continuous delivery pipelines into Jenkins. Pipeline provides an extensible set of tools for modeling simple-to-complex delivery pipelines "as code".

A[`Jenkinsfile`](https://jenkins.io/doc/book/pipeline/jenkinsfile)is a text file that contains the definition of a Jenkins Pipeline and is checked into source control.This is the foundation of "Pipeline-as-Code"; treating the continuous delivery pipeline a part of the application to be version and reviewed like any other code. Creating a`Jenkinsfile `provides a number of immediate benefits:

* Automatically create Pipelines for all Branches and Pull Requests

* Code review/iteration on the Pipeline

* Audit trail for the Pipeline

* Single source of truth for the Pipeline, which can be viewed and edited by multiple members of the project.

While the syntax for defining a Pipeline, either in the web UI or with a`Jenkinsfile`, is the same, it’s generally considered best practice to define the Pipeline in a`Jenkinsfile`and check that in to source control.

##  {#guided-tour}



