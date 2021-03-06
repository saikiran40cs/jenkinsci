### Installation of Jenkins on Tomcat {#install-jenkins}

---

Continuous integration is a process in which all development work is integrated at [](https://rutfin.files.wordpress.com/2012/11/jenkins.png)a predefined time or event and the resulting work is automatically tested and build. The idea is that development errors are identified very early in the process.

**ENVIRONMENT**

* Apache Tomcat 7.0.2 \([Download](http://tomcat.apache.org/download-70.cgi)\)
* JDK 1.6.0\_33 \([Download](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html)\)
* Jenkins 1.475 \([Download](http://jenkins-ci.org/)\)

**INSTALLATION**

**Jenkins can Run as a standalone application:**

_java -jar jenkins.war –httpPort=18080 –ajp13Port=18009_

Jenkins should be available under “[http://localhost:18080/jenkins/&\#8221](http://localhost:18080/jenkins/&#8221);.

**Or deploys in an application server as Tomcat:**

* Copy Jenkins.war as ROOT.war
* Delete all folders in \[$TOMCAT\_HOME\]/webapp
* Copy ROOT.war in the webapp folder
* Modify the file \[$TOMCAT\_HOME\]/conf/context.xml and add the next line:

_&lt;Environment name=”JENKINS\_HOME” value=”\[path\_to\_jenkins\]\.jenkins” type=”java.lang.String”/&gt;_

* Modify the file \[$TOMCAT\_HOME\]/conf/server.xml and in &lt;Connector port=”18080″ add the next parameter URIEncoding=”UTF-8″. Also you can modify the ports if it is required

If you start Tomcat your Jenkins installation should be available under “[http://localhost:18080/&\#8221](http://localhost:18080/&#8221);.

**Tomcat as a service in Windows**

* Run \[$TOMCAT\_HOME\]/bin/service.bat install

* To update the service parameters

> _C:\&gt;   tomcat7 //US//Tomcat7 –DisplayName=”Apache Tomcat 7″ \_
>
> _C:\&gt; –Description=”Apache Tomcat Server – _[_http://tomcat.apache.org/_](http://tomcat.apache.org/)_ “_

![](/assets/jenkins-main.png)



