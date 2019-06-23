pipeline {
    agent any
    stages {
        stage ('init') {
            steps {
                echo "This is Initializing Stage"
                clean pacakage checkstyle:checkstyle
                
            }
        }
        stage ('Build') {
            steps {
                echo "This is build stage"
            }
        }
        stage ('Deploy') {
            steps {
                echo "This is deployment stage"
            }
        }
    }
}