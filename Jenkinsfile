pipeline {
agent any
	stages {
	  stage('demo run linux command') {
	    steps {
			scripts{
			try {
	      		sh '''
	        	pwd 
	        	whoam
	        	uname -a
	      		''' }
			catch (Exception e) {
					echo "Command execution failed: ${e.getMessage()}"
				}
	    }
	  }
	}
}
