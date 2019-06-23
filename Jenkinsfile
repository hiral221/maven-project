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
                sh label: '', script: 'mvn clean package checkstyle:checkstyle'
            }
            post{
                success{
                    echo "shell script maven"
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