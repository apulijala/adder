pipeline{
    agent{
        label "docker"
    }

    stages {
        stage("Compile") {
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



