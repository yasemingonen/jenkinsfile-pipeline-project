pipeline {
    agent any
    
    stage('Checkout') {
        steps {
            git branch: 'main',
                url: 'git@github.com:yasemingonen/jenkinsfile-pipeline-project.git'
        }
    }
    
    stages {
        stage('build') {
            steps {
                echo 'Compiling the java source code'
                sh 'javac Hello.java'
            }
        }
        stage('run') {
            steps {
                echo 'Running the compiled java code.'
                sh 'java Hello'
            }
        }
    }
}
