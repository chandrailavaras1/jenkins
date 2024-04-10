pipeline{
    agent any
    stages{
        stage("hello"){
            steps{
                echo "hello"
            }
        }
        stage("Scripted language"){
            steps{
                script{
                    def course = "k8s"
                    if(course == "k8s")
                        println("Thanks for enrolling ${course}")
                    else
                        println("enroll")
                    sleep 60
                    echo "Script will end here"
                }
            }
        }
    }
}
