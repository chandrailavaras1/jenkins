pipeline{
    agent any
    stages{
        stage("Sample build"){
            steps{
                echo "Sample build"
            }
        }
        stage("when_expression"){
            when{
                expression{
                    BRANCH_NAME ==~ /(production|3)/
                }
            }
            steps{
                echo "This is executed after 1st stage and it is when expression passes"
            }
        }
    }
}
