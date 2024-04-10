pipeline{
    agent any
    stages{
        stage("sample build"){
            steps{
                echo "Sample build is created"
            }
        }
        stage("timeout"){
            steps{
                timeout(time: 5,unit: "SECONDS"){
                    retry(3){
                        echo "Sleeping for 5 seconds"
                        sleep 2
                    }
                }
                echo "This is executed in retry block"
            }
        }
    }
}
