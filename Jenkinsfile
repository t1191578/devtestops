pipeline {
    agent any
    environment {
        PATH = "/usr/share/maven/bin:$PATH"
    }
 
        stage("build code"){
            steps{
              sh "mvn clean install"
            }
        }
        stage("Test"){
            steps{
              sh "mvn test"
            }
        }
        stage("Package"){
            steps{
              sh "mvn package"
            }
        }
        
    }
}
