pipeline {
    agent any 
    stages {
        stage('Clone repo') { 
            steps {
	        	echo 'Cloning ...'
                	sh "git clone https://github.com/pabloccna/java-pipeline-jenkinsfile.git"	
            }
        }
	stage('Build & package') { 
            steps {
		        echo 'MVN pack ...'
                	sh "mvn package"
           }
        }
	    
    }
	post { 
        	always { 
            	cleanWs()
		}
        }
}
