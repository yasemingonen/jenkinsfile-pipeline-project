// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             agent {
//                 docker {
//                     image 'gradle:6.7-jdk11'
//                     // Run the container on the node specified at the top-level of the Pipeline, in the same workspace, rather than on a new node entirely:
//                     reuseNode true
//                 }
//             }
//             steps {
//                 sh 'gradle --version'
//             }
//         }
//     }
// }
pipeline {
    agent any
    tools {
        gradle "Gradle"
    }
    environment {
        GIT_PROJECT_URL = "${GIT_PROJECT_URL}"
        IMAGE_VERSION = "${params.IMAGE_VERSION}"
        }
 options {
    skipDefaultCheckout(true)
 } 
   
// node {
//   withGradle {
//     sh './gradlew build'
//   }
// }

stages { 
    
    stage('Get Source Code') {
            steps {
                checkout scm: [$class: 'GitSCM', userRemoteConfigs: [[url: '${GIT_PROJECT_URL}' ]], branches: [[name: '${IMAGE_VERSION}']]],poll: false
                sh '''#!/bin/bash -e
                #mvn -version
                echo STEP: checkout git scm. Source Code URL: ${GIT_PROJECT_URL}, Source Code Version: ${IMAGE_VERSION} 
                '''
            }
        }
    
    stage('gradle build') {
        steps {
            withGradle {
                sh './gradlew clean build --build-cache --parallel'
             }
         }
     }
}
}

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

