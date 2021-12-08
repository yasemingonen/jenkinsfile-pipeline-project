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
     
       stage ('Build') {
            steps {
                sh './gradlew clean build'
            }
       }
//         stage('Maven Build') {
//             steps {
//                 echo 'Compiling the java source code'
//                 sh 'javac HelloWorld.java'
//             }
//         }
//         stage('Docker Build') {
//             steps {
//                 echo 'Compiling the java source code'
//                 sh 'javac HelloWorld.java'
//             }
//         }
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
