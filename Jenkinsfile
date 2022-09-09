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
                          clean compile package
                          bat "copy "target\java-hello-world.war" "C:\Users\hussa\Desktop\Deploy\apache-tomcat-9.0.64\webapps""
                          bat "cd C:\Users\hussa\Desktop\Deploy\apache-tomcat-9.0.64\bin"
                          bat ".\catalina.bat stop"
                          bat ".\catalina.bat start"

                        }
                 tools {
                         maven 'Maven-3.8.5'
                       }
        }

        }
        
               
    }
}
