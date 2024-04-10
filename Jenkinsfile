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
                    echo "Sleeping for 5 seconds"
                    sleep 60
                }
            }
        }
    }
}
