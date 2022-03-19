pipeline{

    agent {

       docker {
            label 'docker'
            image 'python:3'
       }
    }
    
    stages {
        
        stage("Compile") {
            steps{
                sh 'python3 -m compileall adder.py'
            }
            
        }

        stage("Run"){
            steps{
                sh 'python3 adder.py 3 5'
            }
        }
        
    }
}
