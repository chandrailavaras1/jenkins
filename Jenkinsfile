pipeline{
    agent any
    environment{
        DEPLOY_TO = production
    }
    stages{
        stage("build"){
            steps{
                echo "Sample build created"
            }
        }
        stage(when_anyOf){
            when{
                allOf{
                    branch "product"
                    environment name: "DEPLOY_TO",value: "production"
                }
            }
            steps{
                echo "Sample when_any OF condition"
            }
        }
    }
}
