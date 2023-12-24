pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Manually checkout the code from Git
                git branch: 'main', url: 'https://github.com/hhanae/my_project.git'
            }
        }

        stage('Deploy Locally') {
            steps {
                script {
                    // Copy the files to the local deployment directory
                    bat 'xcopy /Y /E .\\* D:\\Assad\\demo_ansible\\my_project'
                }
            }
        }
    }
}
