pipeline {
    agent any 
    stages {
        stage('Clone repo') { 
            steps {
	        	echo 'Cloning ...'
                	sh "git clone https://github.com/pabloccna/java-pipeline-jenkinsfile.git"	
            }
        }
	stage('Install') { 
            steps {
		        echo 'MVN Install ...'
                	sh "mvn install"
           }
        }
        stage('Build') { 
            steps {
		        echo 'Building ...'
                	sh "javac HelloWorld.java"
           }
        }
	   
	stage('Run') { 
            steps {
                	echo 'Running ...'
	        	sh "java HelloWorld"
            	}
        }
	    
    }
	post { 
        	always { 
            	cleanWs()
		}
        }
}
