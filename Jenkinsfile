pipeline{
    agent any
    environment{
        DEPLOY_TO = "staging"
    }
    stages{
        stage("build"){
            steps{
                echo "Sample build"
            }
        }
        stage("when_not"){
            when{
                not{
                    equals expected: "staging",actual: "${DEPLOY_TO}"
                }
            }
            steps{
                echo "Deploying in Jenkins"
            }
        }
    }
}
