# Prior to the Workshop:
#### (Preferably do before the workshop)

1. Fork this project to your Github Repo
2. Create a Token with the following permission.. Keep this token handy..
repo (all)
admin:repo_hook (read, write)
admin:public_key (read, write)
3. Join us on 22-Aug for session

# On the Day of Workshop 
## Create Integrations
JFrog Pipelines has a concept of Integrations. Integrations allows us to integrate with 2p / 3p tools like AWS, k8s, Github

#### Configure SCM in JFrog Pipeline
1. Login to JFrog Platform
2. Admin > Pipeline > Integration > Add Integration
Name of Integration: ```<yourinitials>_github```

## Pipeline Development Environment (PDE)
PDE is an IDE for JFrog Pipelines. Its being built with the focus to enable building pipelines easily. 
Given that its Alpha, each participant will have to enable it.

### Steps to Enable PDE
1. Login to JFrog Platform
2. F12 (Developer Tools) > Console > ```localStorage.setItem('PDE', true)```
3. Close the Developer Tools

## Create Pipeline Source
This steps is primairly to specify which repo has the YAML for the Pipelines which is being built.
1. Login to JFrog Platform
2. Admin > Pipeline > Integration > Add Integration

## Let the fun begin (Hands-On)

#### Hands-On 1 : Create a Pipeline to do Mvn Build + Docker Build & Publish

--> Step-1
Update values.yaml
var:
  project: <<project which you working on.. no hyphen ("-") use underscore instead "_" in project name>>
  gitProvider: <<integration name you created>>
  path: <<your Github Username>>/pipelines-devnext
  jfrogPlatformInstance: <<devnextsaas1.jfrog.io or devnextsaas2.jfrog.io>>

--> Step-2
Update mvn step command to ```clean install``` 

--> Step-3
Validate

--> Step-4
Save

--> Step-5
Navigate to pipeline a_java_devnext_workshop_1 pipeline


#### Hands-On 2 : Print messages onComplete() & preRun & trigger pipeline

--> Step-1
add echo statements
