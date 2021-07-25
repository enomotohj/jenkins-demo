pipeline{
    agent any
    tools {
        maven "mvn3" 
    }
    stages{
        stage("test"){
            steps{
                sh "mvn clean test"
            }
            post{
                always{
                    echo "========test finished========"
                }
                success{
                    echo "========test successfully========"
                }
                failure{
                    echo "========test failed========"
                }
            }
        }
        stage("build"){
            steps{
                sh "mvn clean package"
            }
            post{
                always{
                    echo "========build finished========"
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