pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3.9.6') {
                    sh 'mvn clean compile'
                }
            }
        }

 //       stage ('Testing Stage') {

//            steps {
  //              withMaven(maven : 'maven_3.9.0') {
    //                sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3.9.5') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
