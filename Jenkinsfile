// 
pipeline {
    agent any
    tools {
        maven 'Maven-3.8.8'
        jdk 'JDK17'
    }
    environment {
        TOMCAT_CREDS = credentials('tomcat_credentials') // jenkins credentials
        NEXUS_VERSION = "nexus3"
        NEXUS_PROTOCOL = "http"
        NEXUS_URL = "34.125.79.139:8081"
        NEXUS_REPO = "new-repo-test"
    }
    stages {
        stage ('clone'){
            steps {
                // clone the repo, go to snippet generator
                git credentialsId: 'github_siva_credentials', url: 'https://github.com/devopswithcloud/spring3-mvc-maven-xml-hello-world.git'
            }
        }
        stage ('Build') {
            steps {
                sh "mvn clean package -Dmaven.test.failure.ignore=true"
                //-Dcheckstyle.skip
            }
            post {
                success {
                    archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
                }
            }
        }
    }
}
