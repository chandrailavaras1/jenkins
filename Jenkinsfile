pipeline{
    agent any
    environment{
        DEPLOY_TO = "prod"
    }
    stages{
        stage("Sample build"){
            steps{
                echo "Sample build"
            }
        }
        stage("when_anyOf"){
            environment{
                DEPLOY_TO_SA = "prod"
            }
            when{
                anyOf{
                    branch "3"
                    environment name: "DEPLOY_TO_SA",value: "prod"
                    expression{
                        BRANCH_NAME ==~ /(prod|2)/
                    }
                }
            }
            steps{
                echo "Sample build created for any Of"
            }
        }
    }
}
