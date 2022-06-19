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
               waitfor SomethingThatIsNeverHappening /t 2
            }
        }
        stage('Integration Test') {
            steps {
               waitfor SomethingThatIsNeverHappening /t 2
            }
        }
        stage('Notify') {
            steps {
               waitfor SomethingThatIsNeverHappening /t 2
            }
        }
    }
}