pipeline {
agent any
	stages {
	  stage('demo run linux command') {
	    steps {
			scripts {
				try { 
					sh "whoam"
					} catch (Exception e) {
					echo "Command execution failed: ${e.getMessage()}"
					}
			}
		}
	  }
	}
}
