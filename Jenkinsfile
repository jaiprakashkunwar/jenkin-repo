pipeline {
    agent any
    stages {
    
        stage('Build') {
            steps {
                bat 'set'
            }
        }
        
        stage('Junit') {
            steps {
                echo"Junit passed successfully"
            }
        }
        
         stage('Deploy') {
            steps {
                echo"Deploy passed successfully"
            }
        }
        
        
    }
    
    post {
        always{
            echo 'This will always run'
        }
        
        success{
            echo 'This will  run only if successful'
           
            
        }
        failure{
            echo 'This will  run only if failed'
        }
        unstable{
            echo 'This will  run only if unstable'
        }
         changed{
            echo 'This will  run only if state of pipeline changed fail <--> successful'
        }

    }

    
}
