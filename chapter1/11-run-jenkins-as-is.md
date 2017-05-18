## Run Jenkins in Seconds

---

1. Run Jenkins with the command`java -jar jenkins.war`.
2. To change the default port of the web interface of Jenkins, use the argument`--httpPort=$port`.  

For example,`java -jar jenkins.war --httpPort=12345`

1. Open url`http://server:port`in browser to configure Jenkins. In the last example, it is`http://localhost:12345`.

2. Download and install plugins following the steps below.

   1. 1. 1. Switch to the`available`tag and search for the plugin. In this example, the`Github Project`plugin is installed to integrate Jenkins with projects on github.

      Click on the`install`button

3. After the installation is finished, you can configure jobs to use existing Github projects.



