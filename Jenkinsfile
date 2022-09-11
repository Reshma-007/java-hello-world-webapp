pipeline {
	agent any 
          tools {
        maven "Maven-3.8.5"
         }
	stages {
	stage ('build'){
		steps {
           		bat 'mvn clean compile package'
            }
		steps {
		bat ''' 
copy "target/java-hello-world.war" "C:/Users/hussa/Desktop/Deploy/apache-tomcat-9.0.64/webapps"
cd C:/Users/hussa/Desktop/Deploy/apache-tomcat-9.0.64/bin
./catalina.bat stop
./catalina.bat start
'''
	}	
	}   
}
}
