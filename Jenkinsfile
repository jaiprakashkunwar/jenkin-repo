pipeline {
    agent any
    stages {
    
        stage('Build') {
        
           environment{
      
               jai_username=credentials('JENKINS_USERNAME');
      
           }
       
            steps {
               // bat 'set'
                  echo'Junit passed successfully $jai_username '
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
