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
                retry(3){
                timeout(time: 5,unit: "SECONDS"){
                    echo "Sleeping for 5 seconds"
                    sleep 10
                }
                echo "This is executed in retry block"
                }
                echo"This is executed everytime"
            }
        }
    }
}
