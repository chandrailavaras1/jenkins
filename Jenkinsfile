pipeline{
    agent any
    environment{
        course = "K8s"
        name = "Chandu"
    }
    stages{
        stage("env_var"){
            steps{
                echo "Welcome ${name}"
                echo "Welcome to ${K8s} course"
            }
        }
        stage("local_env"){
            environment{
                cloud = "GCP"
                course = "Devops"
            }
            steps{
                echo "Welcome to ${cloud} & ${course} course ,${name}"
                echo "This is Second Stage"
            }
        }
    }
}
