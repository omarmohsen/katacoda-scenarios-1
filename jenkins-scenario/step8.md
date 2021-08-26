Now for the most exciting part.

You are going to add a stage to run our appliction.

Add the follwoing stage:

`
		stage ('run python app'){
			steps{
				sh 'python3 manage.py runserver 0.0.0.0:8000 &'
			}
		}
`

Now lets Run the pipeline and test the stages you made.

If it passed, proceed with the next step, if not please troubleshoot and test again.

Lets now access ths URL to check the application on port `8000` [tcp://[[HOST_IP]]:8000/register](tcp://[[HOST_IP]]:8000/register)