pipeline{
    agent any
    environment{
        DEPLOY_TO = "production"
    }
    stages{
        stage("hello"){
            steps{
                echo "Sample file executed"
            }
        }
        stage("deployed to satges"){
            when{
                environment name: "DEPLOY_TO", value: "production"
            }
            steps{
                echo "This is second stage"
            }
        }
    }
}
