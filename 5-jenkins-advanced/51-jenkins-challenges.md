# Jenkins Challenges {#jenkins-documentation}

---

hudson CI: how to delete all jobs?



Q: I have about 100 jobs on my hudson CI, possible to mass delete them ?

A:  The easiest way, IMHO, would be to use script. Go to http://your.hudson.url/script/



Delete jobs by running in Older versions\(1.x\):

> for\(j in hudson.model.Hudson.theInstance.getProjects\(\)\) {
>
>     j.delete\(\);
>
> }



And this way gives you an option to easily use condition to filter out jobs to delete.

FOR JENKINS Current versions \(2.x\):

> for\(j in jenkins.model.Jenkins.theInstance.getAllItems\(\)\) {
>
>     j.delete\(\)
>
> }



Q: How to reset build number in jenkins?

A: Can be easier done from groovy script console . Go to http://your-jenkins-server/script In script window enter:

> item = Jenkins.instance.getItemByFullName\("your-job-name-here"\)
>
> //THIS WILL REMOVE ALL BUILD HISTORY
>
> item.builds.each\(\) { build -&gt;
>
>   build.delete\(\)
>
> }
>
> item.updateNextBuildNumber\(1\)

OR 

> echo "deleting all builds of ${jobName}" item = Jenkins.instance.getItemByFullName\("${jobName}"\) for \(build in item.builds\){ build.delete\(\); } item.updateNextBuildNumber\(1\)



For ALL PROJECTS

> Jenkins.instance.allItems.each\(\) { 
>
>   item -&gt; item.builds.each\(\) { 
>
>     build -&gt; build.delete\(\)
>
>   }
>
>   item.updateNextBuildNumber\(1\)
>
> }



