pipeline {
    agent any
    stages {
        stage("clone the project") {
            steps{
                git "https://github.com/vaadin/addressbook"
            }
        }
        stage("compile"){
            steps{	
		echo "compiling the code"
                sh "mvn compile"
            }
	}            
        stage("tests"){
            steps{
		echo "testing the code"
                sh "mvn test"
            }
		}            
        stage("package"){
            steps{
                sh "mvn package"
            }            
        }
      
    }
}
