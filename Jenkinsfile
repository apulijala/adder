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
                        echo "Parallel Branch A"
                    },
                    b: {
                        echo "Parllel Branch B and B"
                    }
                    )
            }
        }
    }
}