pipeline {
agent any
	stage('Demo commands') {
            steps {
                script {
                    try {
                        
                        sh '''
						echo "Running linux commands"
						whoami
						'''
                    } catch (Exception e) {
                        echo "command is not running: ${e.getMessage()}"
                    }               
                }
            }
        }
}
