pipeline {
    agent any
    environment {
        PATH = "/usr/share/maven/bin:$PATH"
    }
    stages {
        stage("clone code"){
            steps{
               git  url: 'https://github.com/t1191578/devtestops.git'
            }
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
