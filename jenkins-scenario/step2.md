After installing Jenkins, lets access it and configure our environment.

So access it from here:
https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/

First, lets install all the necessary plugins that you will need, to configure and start our pipeline for the application you will run.

You will need to install the following plugins to help you in your pipeline:

- Git

- Pipeline

- Docker

Please follow these steps to install the above plugins:

1- Click `Manage Jenkins` from the left panel.

2- Click `Manage Plugins`.

3- Click `Available` tab.

4- Search for the plugins you want to install, and check their box.

5- Click `Download and restart`.

6- Check the Box `Restart Jenkins when installation is complete and no jobs are running`.


Now you have installed the plugins you will need for creating your pipeline.

Next, you will configure your Jenkins agent so you can specify where to run your pipelines.
