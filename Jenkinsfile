pipeline{
    agent none
    tools {
        maven "mvn3" 
    }
    stages{
        stage("checkout"){
            steps{
                echo "========checkout========"
            }
        }
        stage("build"){
            steps{
                bat "mvn clean package"
            }
            post{
                always{
                    echo "build finished"
                }
                success{
                    echo "========build successfully========"
                }
                failure{
                    echo "========build failed========"
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}