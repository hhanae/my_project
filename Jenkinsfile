pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Manually checkout the code from Git with a specific refspec
                git branch: 'main', credentialsId: '9292958e-c16b-4c59-b7dd-5312aedea6a9', url: 'https://github.com/hhanae/my_project.git'
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
