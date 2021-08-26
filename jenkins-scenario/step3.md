In this step, you will configure your Jenkins agent.

So before diving into the steps, lets know what is meant by `Agent`.

Agent is basically a server where Jenkins creates its wokspace on, to execut the commands in its pipeline.


So follow these steps to configure your agent:

1- Click `Manage Jenkins` from the left panel.

2- Click `Manage Nodes`.

3- Click `New Node`.

4- Give your agent a name, `test`.

5- Select `Permenant Agent`.

6- For `Remote root directory` type `/root`.

7- For `Launch method`, select `Launch agent via ssh`.

8- For `host`, you will need to add the host IP, to get it, execute `ip addr show`{{execute}} and get the IP under `ens3`.

9- Click `Add credentials`.

a- For `Kind`, select `SSH username and private key`.

b- For `Scope`, select `Global`.

c- For `ID`, type `agent`.

d- For `Username`, type `root`.

e- Get the Private key by executing `cat /root/.ssh/id_rsa`{{execute}}.

f- Click `Private Key` check mark, then click `Add` button and add the Private key from the previous step.

10- For `host verification stratgey`, select `none verifying Verification Strategy`.

11- Click `Save`.

12- Click `Ok`.

13- To view the progress, Click you agent you just created, the Click `logs`.

Wait till its succesfuly conneted

Next, you will start creating our pipeline.