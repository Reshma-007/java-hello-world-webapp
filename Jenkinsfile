pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Code') {
            steps {
                echo 'Code'
            }
        }
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('Deploy') {
            steps {
                tools {
                         maven 'Maven-3.8.5'
                      }
                  }
         }
             stages {
                 stage('maven build') {
                  steps {
                          bat 'mvn clean compile package'
                        }
                 tools {
                         maven 'Maven-3.8.5'
                       }
        }

        }
        
               
    }
}
