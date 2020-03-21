pipeline{
	agent any
            stages{
		stage('checkout'){
			steps{
                            sh 'git clone \'https://github.com/edureka-devops/projCert.git\''
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
