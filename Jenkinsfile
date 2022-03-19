pipeline {
    agent{
        label "docker"
    }
    stages {
        stage("Running some command") {

            steps{
                echo "========executing A========"
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
}