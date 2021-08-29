Next you will need to add a stage to install some prerequisites on your machine that will help run your application, since the application is written in python.

So, paste the following as your second stage after the previous one:


`stage ('Install python requirements'){
	steps{
		sh 'pip3 install -r requirements.txt'
	}
}
`		

in the `/root/workspace/django-pipeline/requirements.txt`{{open}} file, you will find a list of packages that python will need to run the Django application

Now lets Run the pipeline and test the stages you made.

If it passed, proceed with the next step, if not please troubleshoot and test again.
