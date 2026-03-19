pipeline {
agent any
	stage('Demo commands') {
            steps {
                script {
                    try {
                        echo "Running linux commands"
                        sh '''
						whoami
						'''
                    } catch (Exception e) {
                        echo "command is not running: ${e.getMessage()}"
                    }               
                }
            }
        }
}
