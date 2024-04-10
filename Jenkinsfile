pipeline{
    agent any
    stages{
        stage("hello"){
            steps{
                echo "Sample step"
            }
        }
        stage("retry"){
            steps{
                retry(3){
                    echo "Welcome to Jenkins"
                    //error "testing retry"
                }
                echo "after retry block"
            }
        }
    }
}
