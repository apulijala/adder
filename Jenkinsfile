pipeline{
    agent{
        label "docker"
    }

    stages {
        stage("Compile"){
            steps{
                echo "========executing A========"
            }
            parallel (
                win: {
                    node("east") {
                        echo "Running windows parallely"
                    }
                },

                liunx: { node ("docker") {
                        echo "In the docker world "
                    }
                }
        )

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
    }
}



