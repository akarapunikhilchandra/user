#!groovy
// it means the libraries will be downloaded and accessible at run time
@Library ('roboshop-shared-library') _

def configMap = [
    application: "nodeJSEKS",
    component: "user"
]
env

// this is .groovy file name and function inside it
// pipelineDecission.decidePipeline(configMap)
if ( ! env.BRANCH_NAME.equalsIgnoreCase('master')){
    pipelineDecission.decidePipeline(configMap)
}
else{
    echo "master PROD deployment should happen through CR"
}