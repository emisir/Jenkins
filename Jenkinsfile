pipeline {
    agent any
    stages {
        stage('Build & Test') {
            steps {
                bat ".\\gradlew.bat build"
            }
        }
        stage('Deploy') {
            steps {
                dir(".\\lib\\build\\libs"){
                    bat "set BUILD_ID=dontKillMe"
                    bat "@start \"\" cmd /c javaw -jar .\\lib-0.0.1-SNAPSHOT.jar"
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