### Run Single Job at same time in multiple machines for the created project {#create-jobs}

---

There are two ways to accomplish this 

1. Using Node Label Parameter plug-in

2. Using Multi- Configuration project + Axis plug-in



1. **Node Label Parameter plug-in :** Install the plug-in, under 'this build is parameterized option', you will find an option for specifying a list of Nodes as a drop down, and then to execute them serially or execute them on multiple nodes parallely, when you select Build option.

2. **Multi-Configuration and Axis Plug-in :** Install both these plug-ins. Create Multi-configuration Jenkins job and then you can create a virtual matrix where the job can run the job on all the nodes identified by a common label. \(You need to specify the common label name in all the nodes created \(Manage nodes --&gt; Node name --&gt; Configure\)\)



Below is the process to run a single job using Node Label Parameter plug-in

**Pre-Requisite Step**− Once the build is scheduled, it will run. The following Build history section shows that a build is in progress.

**Step 1**− Once the build is scheduled, it will run. The following Build history section shows that a build is in progress.

**Step 2**− Once the build is completed, a status of the build will show if the build was successful or not. In our case, the following build has been executed successfully. Click on the \#1 in the Build history to bring up the details of the build.

**Step 3**− Click on the Console Output link to see the details of the build running a Single Job simultaneously in Multiple slaves

