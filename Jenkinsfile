pipeline {
    agent any
  
    tools {nodejs "NodeJS"} 
  
    stages {
      
        stage ('Build') {
            steps {
                echo 'Building dependencies...'
      			sh 'npm cache verify'
				sh 'npm install'
				sh 'npm install -g @angular/cli'
				sh 'ng build'
            }
        }
        

        stage ('Unit Test') {
            steps {
                sh 'ng test' 
            }
        }     
      
        stage ('Code Coverage') {
            steps {
                sh 'ls' 
            }
        }
        
        stage ('Sonarcube') {
            steps {
                sh 'ls' 
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
            }
        }  
    } // end stages
    
    post {
        always {
        }
    }
}
