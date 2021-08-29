In this step, you will configure a stage to run unit test on the code you cloned from the repository.


`stage ('run tests'){
	steps{
		sh 'python3 manage.py test blog'
	}
}
`		
Now lets Run the pipeline and test the stages you made.

If it passed, proceed with the next step, if not please troubleshoot and test again.
