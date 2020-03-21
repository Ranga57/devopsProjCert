pipeline{
	agent any
            stages{
		stage('checkout'){
			steps{
			    sh rm - R /var/lib/jenkins/workspace/devopsCertproj/*
                            sh 'git clone \'https://github.com/gabrielf/maven-samples.git\''
			}			
		}
		stage('build'){
			steps{
			sh 'mvn compile'
			}			
		}
		stage('Test') {
	            steps {
        	        sh 'mvn test'
            	    }
            	    post {
                	always {
                    	   junit 'target/surefire-reports/*.xml'
            	        } 
                    }
	        } 
	  }
}
