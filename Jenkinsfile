pipeline {
    agent any

    stages {
        stage ('Compile stage'){
            steps{
               withMaven(maven : '3.5.2'){
                    sh 'mvn clean compile'
                }
            }
        }
         stage ('Testing stage'){
                    steps{
                       withMaven(maven : '3.5.2'){
                            sh 'mvn test'
                        }
                    }
         }
          stage ('Deploy stage'){
                     steps{
                        withMaven(maven : '3.5.2'){
                             sh 'mvn deploy'
                         }
                     }
          }
    }
}