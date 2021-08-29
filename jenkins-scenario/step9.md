In this step, we will add a stage to run the image we made in the previous one

Add the following stage:


`stage ('Run docker container'){
	steps{
		sh 'docker run --rm  -d -p 8001:8000 django-blog'
	}
}
`

Now lets Run the pipeline and test the stages you made.

Now check your container if its running by executing `docker ps`{{execute}}

If it passed, proceed with the next step, if not please troubleshoot and test again.

Lets now access this URL to check the application on port `8001` [tcp://[[HOST_IP]]:8001/register](tcp://[[HOST_IP]]:8001/register)
