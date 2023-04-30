pipeline{
    
    agent any 
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                                
                    git branch: 'main', credentialsId: '1fcd2439-07b2-41b2-801a-66cc7c346402', url: 'https://github.com/Mubarak756/demo-counter-app.git'
                }
            }
            
        stage('Unit Testing'){
            
            steps{
			
                sh 'mvn test'
           }      
        }
		stage('Integration Testing'){
            
            steps{
			
                sh 'mvn verify -DskipUnitTests'
			}	
        } 
		stage('Maven Build'){
            
            steps{
			
                sh 'mvn clean install'
            }
		}
	}        
  }
