pipeline {
    agent{
        label "docker"
    }
    stages {
        stage("Running some command") {
            steps{
                echo "========executing A========"
                script {
                    def response = input id: 'Approver', message: 'Om Aim Hreem Shreem Kleem Shree Mathre Namaha', ok: 'Approve it', submitterParameter: 'approver'
                    echo "${response}"

                }
                
                
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