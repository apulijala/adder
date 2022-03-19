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

        parallel {
                stage('Test On Windows') {
                    agent {
                        label "docker"
                    }
                    steps {
                        echo "Running on Windows"
                    }
                    post {
                        always {
                            echo "Running Always on Windows"
                        }
                    }
                }
                stage('Test On Linux') {
                    agent {
                        label "docker"
                    }
                    steps {
                        echo "Running on Linux"
                    }
                    post {
                        always {
                            echo "Running always on Linux"
                        }
                    }
                }
            }
        }
}