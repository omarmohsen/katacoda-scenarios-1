For the last step, we will add a stage to push the image we have to Docker Hub.

So, paste the following as your second stage after the previous one:


		`stage ('run docker container'){
			steps{
				script {						
					withCredentials([usernamePassword(credentialsId: 'summeracademyid', passwordVariable: 'password', usernameVariable: 'username')]) { //recall the credentials we added
						sh "docker login -u $username -p $password <your-dockrhub-username>"																		//login to dockrhub account
					}
				sh 'docker tag django-blog <your-dockrhub-username>/django-blog'																					// change the name of the image to match your DockerHub username
				sh 'docker push <your-dockrhub-username>/django-blog'																								//push the image
			}
		}
		`

Now lets Run the pipeline and test the stages you made.

If it passed, proceed with the next step, if not please troubleshoot and test again.

No you may check your Docker Hub account for your image.
