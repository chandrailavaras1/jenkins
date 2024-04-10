pipeline{
    agent any
    stages{
        stage("Sample"){
            steps{
                echo "This is sample build"
            }
        }
        stage("Creds"){
            environment{
                GITHUB_CREDS = credentials("github_creds")
            }
            steps{
                echo "Github creds ${GITHUB_CREDS}"
                echo "Github username ${GITHUB_USR}"
                echo "Github password ${GITHUB_PSW}"
            }
        }
    }
}
