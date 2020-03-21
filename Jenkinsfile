pipeline{
	agent none

		stages('checkout'){
			step{
                            sh git clone 'https://github.com/edureka-devops/projCert.git'
			}			
		}
		stages('build'){
			step{
			sh mvn compile
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
