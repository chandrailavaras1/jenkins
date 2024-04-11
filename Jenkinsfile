pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Sample build"
            }
        }
        stage("paralleljobs"){
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
        }
        stage ('Deploy') {
            steps {
                echo "Deploying to env"
            }
        }
    } 
}
