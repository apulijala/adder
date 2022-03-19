pipeline {
    agent{
        label "docker"
    }
    stages {
        stage("Running some command") {
            steps{
                echo "========executing A========"
                input id: 'ctns-prompt', message: 'Do You want to proceed to next stage ? '
            }

            
        }
        
        stage('run-parallel-branches') {
            agent {
                label "docker"
            }
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