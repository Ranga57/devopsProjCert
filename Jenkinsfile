pipeline{
	agent none
            stages{
		stage('checkout'){
			step{
                            sh git clone 'https://github.com/edureka-devops/projCert.git'
			}			
		}
		stage('build'){
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
}
