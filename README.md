# Exploring Appflow Exercise 5 

This part -5 of the exploring Appflow exercise consists of the following topics (Available for only Growth and above plans

1. Automations
2. Native Configurations
3. Scripting and Environments

## Automations
Now that you are well versed with triggering different builds in appflow it's time to automate builds.

You can leverage the automation available in a appflow dashboard to automatically trigger the different builds on commit to you Git.

Automations enable you and your team to utilize the full CI/CD powers of Appflow. You can create automations that trigger package builds and deploy builds every time your team checks in new code to a given branch and you can even configure the automations to use different environments and native configurations so that you can build different versions of your app for development, staging, and production.

### Creating an Automation
Let's create an automation for Android Debug build that you already manually triggered earlier.

Since we were able to successfully build an Android binary using Package, we can now create an automation that triggers an Android Debug build every time a developer pushes code to the development git branch. This way the entire team can easily see when the builds break and track down the exact commit for fast and efficient debugging.

To get started, navigate to the Automate tab within the desired app and click the New Automation button in the top right.

![Appflow](images/img5_1.png)

Next, fill in the configuration options:

* **Name:** The name of the automation.
* **Git Branch:** The branch you'd like to trigger the automation from (ex: master). Note: The asterisk (\*) is a wildcard and will match anything.
* **Automation Type:**  Since, we are doing automation for android, select Package build.
* **Environments:** You can include any enviroments that can be used by this automations. Donot select any environments for now.
* **Native configuration:** You can include any Native configuration that can be used by this automations. Donot select any Native configuration for now.

![Appflow](images/img5_2.png)

### Testing an Automation

Now that the automation is created, any time a developer pushes to the master branch for this application, a new Android Debug type build will automatically start. Simply push a new commit to your master branch to try out the automation.

You can view all the builds associated with a particular automation by navigating to the Automations page in the Appflow Dashboard and clicking the automation from the list.

Try making a trivial change and push to git and the automation should trigger a new build.

### Native Configurations



