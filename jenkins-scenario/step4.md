Now you are ready to create the pipeline.

You wont have to know the syntax of the pipeline, thats not the purpose of this scenario.

you will give you the synatx to paste it and describe in details what exactly this does.

So follow these steps to create your pipeline:

1- Click `New Item`.

2- Select `Pipeline`.

3- Give it a name, `django-pipeline`.

4- Click `Ok`, this will open a new page for you.

5- Scroll to the bottom to the `Pipeline` section, this is where you will type your groovy code in.

6- Paste the follwoing in the `Pipeline` section, this is the basic structure of the pipeline.

```
pipeline {
    
  agent {                       //this is where you specify your agent name
    node {
      label 'test'              //put your agent name betyouen these 2 quoets
    }
  } 

	stages {                    //declare that this is the stages that the pipeline will executes its commands, it may containe as much stages as you will need.
		stage (''){             //declare your first stage.
			steps{              //where you will type the commands that will be executed.
				
			} 
		}			
		stage (''){
			steps{
				
			}
		}
	}
}
```

This is the basic structure of our pipeline, you will modify it as you proceed with the upcomming steps.