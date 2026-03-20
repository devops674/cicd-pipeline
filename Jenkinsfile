pipeline {
    agent any

    stages {
        stage('Clone Project') {
            steps {
                echo 'Cloning the project from Github'
                git branch: "main", url: "https://github.com/ura-vf4/crypto-tax-calculator.git"
            }
        }
        stage('Install Py Sonar') {
            steps {
                echo 'Install pysonar using pip'
                sh """
                sudo pip3 install pysonar --break-system-packages
                """
            }
        }
        stage('Scan the code with pysonar') {
            steps {
                echo 'Running PySonar...'
                sh """
                sudo pysonar --sonar-host-url=http://15.206.122.81:9000 --sonar-token=sqp_e05d33feff6b0e0ce14d63dbc5a4ad43d4948636 --sonar-project-key=DevSecOps_project_CI
                """
            }
        }
    }
}
