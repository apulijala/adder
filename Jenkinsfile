pipeline {

    agent {
       dockerfile {
            label 'docker'
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

        stage("Unit Test") {
            steps {
             
                sh '''python3 -m pytest \
                    -v --junitxml=junit.xml \
                    --cov-report xml --cov adder adder.py
                    '''
            }

            steps {
            
                echo "Sree Gurobhyo Namaha !!"
                echo "Om Aim Hreem Shreem Kleem Shree Mathre Namaha !!"

            }

            post {
                    always {
                        echo "Trigger the Build"
                        junit 'junit.xml'
                        cobertura  coberturaReportFile: 'coverage.xml', conditionalCoverageTargets: '70, 0, 0', failUnhealthy: false, failUnstable: false, lineCoverageTargets: '80, 0, 0', maxNumberOfBuilds: 0, methodCoverageTargets: '80, 0, 0',  zoomCoverageChart: false
                        echo "Built all the files"
                    } 
            }
        }

    }
}