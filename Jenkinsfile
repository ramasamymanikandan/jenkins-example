pipeline {
    agent any

    tools {
        maven 'maven_3_5_0'  // Ensure Maven is correctly configured
    }

    stages {
        stage('Compile Stage') {
            steps {
                script {
                    withMaven(maven: 'maven_3_5_0') {
                        sh 'mvn clean compile'
                    }
                }
            }
        }

        stage('Testing Stage') {
            steps {
                script {
                    withMaven(maven: 'maven_3_5_0') {
                        sh 'mvn test'
                    }
                }
            }
        }

        stage('Deployment Stage') {
            steps {
                script {
                    withMaven(maven: 'maven_3_5_0') {
                        sh 'mvn deploy'
                    }
                }
            }
        }
    }
}
