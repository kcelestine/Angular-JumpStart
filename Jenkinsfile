pipeline {
    agent any
  
    tools {nodejs "node"} 
  
    stages {
      
        stage ('Build') {
            steps {
                echo 'Building dependencies...'
      			sh 'npm cache verify'
				sh 'npm install'
				sh 'npm install -g @angular/cli'
        // sh ' npm i -D @angular-devkit/core '
				sh 'ng build'
            }
        }
        

        stage ('Unit Test') {
            steps {
                sh 'ng test --code-coverage' 
                sh 'ls'
            }
        }     

        
        stage ('Sonarcube') {
            steps {
               sh 'ls' 
                //sonar-scanner -Dsonar.projectKey=front-end -Dsonar.organization=kcelestine-github -Dsonar.sources=. -Dsonar.host.url='https://sonarcloud.io' -Dsonar.login=b259b52022644f00916718a2f7c10446380c5702
            }   
        }        
        stage ('Deploy to Dev') {
            steps {
                sh 'ls' 
            }
        }  
        
        stage ('E2E Test') {
            steps {
                sh 'ls' 
            }
        }  
        
        stage ('Smoke Test') {
            steps {
                sh 'ls' 
                sh 'ls coverage'
            }
        }  
    } // end stages
    
    post {
        always {
          steps { 
            sh 'ls'
          }
        }
    }
}
