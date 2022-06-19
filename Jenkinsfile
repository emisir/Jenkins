pipeline {
    agent any
    stages {
        stage('Build & Test') {
            steps {
                dir("~"){
                    bat "echo %cd&"
                }
                bat ".\\gradlew.bat build"
            }
        }
        stage('Deploy') {
            steps {
                dir(".\\lib\\build\\libs"){
                    bat "copy .\\lib-0.0.1-SNAPSHOT.jar ~\\deployment"
                }
            
                dir("~\\deployment"){
                    bat "java -jar .\\lib-0.0.1-SNAPSHOT.jar"
                }
            }
        }
        stage('Integration Test') {
            steps {
                sleep(time:3,unit:"SECONDS")
            }
        }
        stage('Notify') {
            steps {
                sleep(time:3,unit:"SECONDS")
            }
        }
    }
}