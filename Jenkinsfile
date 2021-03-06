pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/RevanthTiruveedhi/PythonFlaskApp.git']]])
                git branch: 'main', url: 'https://github.com/RevanthTiruveedhi/PythonFlaskApp.git'                                
                sh 'python -m py_compile app.py'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo working' 
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo deployworking'
            }
        }
    }
}
