# jenkins_concepts

Earlier, Jenkins use to work in master and worker node setup. 
Where master used to manage request, and worker nodes were used to execute.

But this was very inefficient way of managing resources as different environment and 
different nodes had to be created and maintained. (wasting resources)

Hence, with the coming up of microservices and docker, Jenkins is now used with Docker
plugin (agent) and the Jenkins Pipelines are now run in Docker containers instead of worker node

# Pipeline Approach

Here instead we selectingg everything in Jenkins (freestyle) we can have a script, where we can define all the build stages and configuration, and simply upload it to any version control system (git). This way we don't have to manually interfere everytime. 

## Stages in pipeline

The steps that have to take place can be mentioned in stages which will be executed one after the other
For example 'Build', 'Test' etc. There can be multiple stages in one pipeline

### Steps 

Inside a stage, we can define multiple steps, steps are the commands which are going to be 
executed in that stage
Jenkins also helps generating script through the generate script for steps 

## Pipleine script from SCM

Instead of writing the pipeline script in Jenkins, we can choose to give Jenkins link to the `JenkinsFile` in a source code management platform like `git` 
We can mention the URL of the repo, mention the branch, and mention the path to the jenkinsfile
