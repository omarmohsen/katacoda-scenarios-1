For the first stage, you will need to clone the reposatory where our application wll be.

So, as your first stage, you will need to paste the follwong:

`
		stage ('clone '){
			steps{
				git url: 'https://github.com/omarmohsen/django-blog'
			} 
		}
`

this stage will clone or download the files and directories on this repo to the jenkins workspace.


Now, Lets test the stage you made:

1- after completing your code, click `Save`.

2- On the left panel, click `Build Now`, this will start your pipeline.

3- See how it goes, if its green then you did it right, if it turns red means that you did something wrong and you will have to revisit your code.

4- If it runs successfully (green), skip this step, and in case its red you may find where is the error by doing the follwong:

    a- In `Build Histroy` secton on the bottom left, click on the failed red build.

    b- Click `Console output`, this will open the log where jenkins ran and failed, troubleshoot and fix your error.

5- Now lets check our clonned reposatory on the workspace, `ls -ltr /var/lib/jenkins/workspace/django-pipeline`{{execute}}, you should see the contents of the reposatory on your workspace.

Lets proceed with the next stage.