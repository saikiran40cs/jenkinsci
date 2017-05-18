## Configure TestNG with Jenkins {#during-analysis}

---

TestNG plugin allows you to publish TestNG results generated using `org.testng.reporters.XMLReporter`.  
TestNG result xml file contains more information than the junit report xml file . This plugin exposes those extra information in graph and table reports.It makes possible to import TestNG XML reports from each build into Jenkins.

The data is parsed using the output generated using **`org.testng.reporters.XMLReporter`**. The results are displayed with a trend graph and all details about which tests that failed are also presented.



The first thing that needs to be done is to install the TestNG plugin into Jenkins, to do this:

1. Open Jenkins in a browser

2. On the Welcome screen click on the "Manage Jenkins" link

3. Click on the "Manage Plugins" link

4. On the Plugin Manager screen click on the "Available" tab

5. Scroll down to find the "**TestNG**" plugin, check the box beside it and click the "**Download now and install after restart**" button

6. Once Jenkins has restarted, click on the "Installed" tab and you will see that the TestNG plugin is now installed.

7. Click on the "Restart Once No Jobs Are Running" button

8. This completes the installation of the TestNG plugin.



