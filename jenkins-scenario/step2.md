After installing Jenkins, lets access it and configure our environment.

So access it from here, choose port 8080:
 [ACCESS PORTS]({{TRAFFIC_SELECTOR}})

First, we need to fix the proxy error:

1- Click `Manage Jenkins`

2- Click `Security`

3- Choose `Default Crumb Issuer`

4- Check `Enable proxy compatability` and Save

Second, lets install all the necessary plugins that you will need, to configure and start our pipeline for the application you will run.

You will need to install the following plugins to help you in your pipeline:

- Git

- Pipeline

- Docker

Please follow these steps to install the above plugins:

1- Click `Manage Jenkins` from the left panel.

2- Click `Manage Plugins`.

3- Click `Available` tab.

4- Search for the plugins you want to install, and check their box.

5- Click on  `Install`.



Now you have installed the plugins you will need for creating your pipeline.

Next, you will configure your Jenkins agent so you can specify where to run your pipelines.
