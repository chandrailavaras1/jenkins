pipeline{
    agent any
    tools{
        maven "Maven"
    }
    stages{
        stage("Sample"){
            steps{
                echo "Sample file executed"
                sh "mvn -version"
            }
        }
        stage("tools"){
            tools{
                jdk "JDK17"
            }
            steps{
                sh "mvn -version"
                echo "This is builded in Java 17th Version"
            }
        }
    }
}
