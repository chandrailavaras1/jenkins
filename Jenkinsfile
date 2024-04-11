pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Sample build"
            }
        }
        stage("parallel_jobs"){
            parallel{
                stage("sonar"){
                    steps{
                        echo "sonar scans"
                        sleep 10
                    }
                }
                stage("fortify"){
                    steps{
                        echo "sonar scans"
                        sleep 10
                    }
                }
                stage("trivy"){
                    steps{
                        error "Sample file"
                        echo "sonar scans"
                        sleep 10
                    }
                }
            }
            steps{
                echo "This si sscanning stage"
            }
        }
    }
}
