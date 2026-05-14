@Library('jenkins-shared-library-for-roboshop')

// create variable of map type and set the values
def configMap = [
    //type: "nodejsEKS",
    component: "catalogue",
    project: "roboshop"
]
echo "test:"

//If it is not main branch, its is feature branch then process it.
if( ! env.BRANCH_NAME.equalsIgnoreCase('main')){
      nodeJSEKSPipeline(configMap)
    //pipelineDecision.decidePipeline(configMap)
}
else{
    //If it is main branch then need to processed with CR process.
    echo "Proceed with CR or NON-PROD pipeline"
}