pipeline {
    agent any
 options {
    skipDefaultCheckout(true)
 }    
 stages { 
        stage('Test Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Maven Build') {
            steps {
                echo 'Compiling the java source code'
                sh 'javac Hello.java'
            }
        }
        stage('Docker Build') {
            steps {
                echo 'Compiling the java source code'
                sh 'javac Hello.java'
            }
        }
//         stage('Docker Push') {
//             steps {
//                 echo 'Compiling the java source code'
//                 sh 'javac Hello.java'
//             }
//         }
//         stage('Helm Upgrade') {
//             steps {
//                 echo 'Running the compiled java code.'
//                 sh 'java Hello'
//             }
//         }
    }
}
