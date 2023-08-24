In this step, you will configure your Jenkins agent.

So before diving into the steps, lets know what is meant by `Agent`.

Agent is basically a server where Jenkins creates its workspace on, to execute the commands in its pipeline.


So follow these steps to configure your agent:

1- Install Java on your machine which is a  dependency for the jenkins agent to work:

`sudo apt install openjdk-11-jre`{{execute}}

2- Click `Manage Jenkins` from the left panel.

3- Click `Nodes`.

4- Click `New Node`.

5- Give your agent a name, `test`.

6- Select `Permanent Agent`.

7- For `Remote root directory` type `/root`.

8- For `Launch method`, select `Launch agent via ssh`.

9- For `Host`, you will need to add the host IP, retrieve the IP from the 2nd network interface (starts with en):

`ip a`{{execute}}

10- Click `Add credentials`.

a- For `Kind`, select `SSH username and private key`.

b- For `Scope`, select `Global`.

c- For `ID`, type `agent`.

d- For `Username`, type `root`.

e- Get the Private key by executing `cat /root/.ssh/id_rsa`{{execute}}.

f- Click `Private Key` check mark, then click `Add` button and add the Private key from the previous step.

11- Choose the credential that you created from the drop down.

12- For `host verification strategy`, select `None verifying`.

13- Click `Save`.

14- To view the progress, Click you agent you just created, the Click `logs`.

Wait till its successfully connected.

Next, you will start creating our pipeline.
