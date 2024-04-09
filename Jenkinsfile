pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
                // Use Maven 3.9.6 for compilation
                withMaven(maven: 'maven_3.9.6') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage('Testing Stage') {
            steps {
                // Use Maven 3.9.0 for testing
                withMaven(maven: 'maven_3.9.0') {
                    sh 'mvn --version'
                    sh 'mvn test'
                }
            }
        }

        stage('Deployment Stage') {
            steps {
                // Use Maven 3.9.5 for deployment
                withMaven(maven: 'maven_3.9.5') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
