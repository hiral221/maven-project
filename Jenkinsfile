pipeline {
    agent any
    stages {
        stage ('init') {
            steps {
                echo "This is Initializing Stage"
                
            }
        }
        stage ('Build') {
            steps {
                echo "This is build stage"
                clean pacakage checkstyle:checkstyle
            }
        }
        stage ('Deploy') {
            steps {
                echo "This is deployment stage"
            }
        }
    }
}