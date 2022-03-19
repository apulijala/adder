pipeline{
    
    agent{
        label "docker"
    }
    
    stages {
        
        stage("A"){
            steps {
                echo "========executing A========"
            }
            steps {
                echo "Jaya Guru Datta"
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
        stage('run-parallel-branches') {
            steps {
                parallel(
                a: {
                    echo "This is branch a"
                },
                b: {
                    echo "This is branch b"
                }
                )
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