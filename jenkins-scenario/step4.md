Now you are ready to create the pipeline.

You wont have to know the syntax of the pipeline, thats not the purpose of this scenario.

you will give you the syntax to paste it and describe in details what exactly this does.

So follow these steps to create your pipeline:

1- Click `Dashboard`.

2- `New Item`.

3- Select `Pipeline`.

4- Give it a name, `django-pipeline`.

5- Click `Ok`, this will open a new page for you.

6- Scroll to the bottom to the `Pipeline` section, this is where you will type your groovy code in.

7- Paste the following in the `Pipeline` section, this is the basic structure of the pipeline.


```
pipeline {
  agent { //Agent name specification
    node {
      label 'test' //Specify agent name
    }
  }

  stages { //State stages of pipeline
    stage('') { //Declare your first stage. (all stages must be inside the stages block)
      steps { //Declare your first stage. (all stages must be inside the stages block)
      }
    }
    stage('') {
      steps {}
    }
    stage('') {
      steps {}
    }

    stage('') {
      steps {}
    }

    stage('') {
      steps {}
    }
  }
}


```


This is the basic structure of our pipeline, you will modify it as you proceed with the upcoming steps.
