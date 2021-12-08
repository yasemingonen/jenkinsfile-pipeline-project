pipeline {
    agent any
 options {
    skipDefaultCheckout(true)
        }    
 stages { 
//         stage('Checkout') {
//           steps {
//               git branch: 'main',
//                   url: 'git@github.com:yasemingonen/jenkinsfile-pipeline-project.git'
//           }
//         }
  
        stage('However I want to name a stage') {
            steps {
                checkout scm
            }
        }
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
