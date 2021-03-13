pipeline {
    agent any

    environment {
        DOTNET_BUILD = 'true'
        DB_BUILD    = 'false'
    }

    stages {
    
            
        stage('Build') {
        
           environment{
      
               jai_username=credentials('JENKINS_USERNAME');
      
           }
       
            steps {
               // bat 'set'
               echo"DOTNET BUILD IS TRUE"
                  echo'Junit passed successfully $jai_username '
                    echo'JENKIN USER NAME $jai_username_USR'
                    echo'JENKIN USER PASS $jai_username_PSW'
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
