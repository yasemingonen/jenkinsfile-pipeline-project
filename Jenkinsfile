pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'gradle:6.7-jdk11'
                    // Run the container on the node specified at the top-level of the Pipeline, in the same workspace, rather than on a new node entirely:
                    reuseNode true
                }
            }
            steps {
                sh 'gradle --version'
            }
        }
    }
}




// pipeline {
//     agent any
//     tools {
//         gradle "Gradle"
//     }
//  options {
//     skipDefaultCheckout(true)
//  } 
    
// node {
//   withGradle {
//     sh './gradlew build'
//   }
// }

// stages { 
//     stage('gradle build') {
//         steps {
//             withGradle {
//                 sh './gradlew build'
//              }
//          }
//      }
// }
// }

//        stage ('Build') {
//             steps {
//                 sh './gradle clean build'
//             }
//        }
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

