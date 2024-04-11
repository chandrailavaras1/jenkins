pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Sample build"
            }
        }
        stage("when_tag"){
            when{
                anyOf{
                    branch "6"
                    expression{
                        TAG_NAME ==~ /(v1.0|v1.2.0)/
                    }
                }
            }
            steps{
                echo "Sample build creadted with any OF condition"
            }
        }
        stage("prod"){
            when{
                tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}",comparator: "REGEXP"
            }
            steps{
                echo "Sample build from tag"
            }
        }
    }
}
