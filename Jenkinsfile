pipeline {
    agent any
    tools {
                    maven'maven3'
                    jdk'java8'
                                    }
    stages {
        stage ('init') {
            steps {
                echo "This is Initializing Stage"
                
            }
        }
        stage ('Build') {
            steps {
                echo "This is build stage"

            }
            post{
                success{
                    echo "shell script maven"
                    sh label: '', script: 'clean package checkstyle:checkstyle'
                    echo "Archive Effect"
                    archiveArtifacts '**/*.war'
                    echo "Junit Job details"
                    junit '**/surefire-reports/*.xml'
                }
            }

        }
        stage ('Deploy') {
            steps {
                echo "This is deployment stage"
            }
        }
    }
}