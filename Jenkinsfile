pipeline{
    agent any
    environment{
        DEPLOY_TO = "prod"
    }
    stages{
        stage("Build"){
            steps{
                echo "Sample build"
            }
        }
        stage("when_tag"){
            when{
                anyOf{
                    environment name: "DEPLOY_TO",value: "prod"
                    expression{
                        BRANCH_NAME ==~ /(prod|4)/
                    }
                }
            }
            steps{
                echo "Sample build creadted with any OF condition"
            }
        }
        stage("prod"){
            when{
                buildingTag()
            }
            steps{
                echo "Sample build from tag"
            }
        }
    }
}
