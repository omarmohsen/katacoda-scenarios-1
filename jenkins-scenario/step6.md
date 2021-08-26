Next you will need to add a stage to install some prerequisits on your machine that will help run your application, since the application is written in python.

So, paste the follwong as your second stage after the prevous one:

`
		stage ('Install python requirements'){
			steps{
				sh 'pip3 install -r requirements.txt'
			}
		}
`

in the `/var/lib/jenkins/workspace/django-pipeline/requirments.txt`{{open}} file, you will find a list of packages that python will need to run the Django application

Now lets Run the pipeline and test the stages you made.

If it passed, proceed with the next step, if not please troubleshoot and test again.