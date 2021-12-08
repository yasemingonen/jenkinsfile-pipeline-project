pipeline {
    agent any
    
    stage('Checkout external proj') {
        steps {
            git branch: 'main',
                url: 'git@github.com:yasemingonen/jenkinsfile-pipeline-project.git'

            sh "ls -lat"
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
