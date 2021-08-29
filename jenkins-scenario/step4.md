Now you are ready to create the pipeline.

You wont have to know the syntax of the pipeline, thats not the purpose of this scenario.

you will give you the syntax to paste it and describe in details what exactly this does.

So follow these steps to create your pipeline:

1- Click `New Item`.

2- Select `Pipeline`.

3- Give it a name, `django-pipeline`.

4- Click `Ok`, this will open a new page for you.

5- Scroll to the bottom to the `Pipeline` section, this is where you will type your groovy code in.

6- Paste the following in the `Pipeline` section, this is the basic structure of the pipeline.


```
pipeline {
  agent {                       //Agent name specification
    node {
      label 'test'              //Specify agent name
    }
  }
       }
	   stages {                    //State stages of pipeline
		stage (''){             //Declare your first stage. (all stages must be inside the stages block)
			steps{              //Block containing steps to be executed
			}
		}
		stage (''){
			steps{
			}
		}
	}
    }




This is the basic structure of our pipeline, you will modify it as you proceed with the upcoming steps.
