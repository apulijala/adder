pipeline {
    agent{
        label "docker"
    }
    stages {
        stage("Running some command") {
            steps{
                echo "========executing A========"
                input message: 'Do you want to Continue ? ', submitterParameter: 'approver'
                echo "Answered By " + resp['approver']
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