Running the application directly on the host is not the best practice, its better to run on a container, and thats what we are going to do in this step.

So, we will subistitute the `run python app` stage with the follwong:

`
		stage ('Build docker image'){
			steps{
				sh 'docker build -t django-blog -f docker/Dockerfile . '
			}
		}
`

This stage will build a Docker container for the application with the `/var/lib/jenkins/workspace/django-pipeline/docker/Dockerfile`{{open}}

Now lets Run the pipeline and test the stages you made.

Also you may check your image is created by excecuting `docker image`{{execute}}

If it passed, proceed with the next step, if not please troubleshoot and test again.