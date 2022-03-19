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

        stage("Running Paallel") {

            parallel {
                stage("Running first command") {
                    agent {
                        label "docker"
                    }
                    steps {
                        echo Running first parallel step 
                    }
                }

                stage("Running second command") {
                    agent {
                        label "docker"
                    }
                    steps {
                        echo Running second parallel step
                    }
                }
            }
        }


        
    }

}