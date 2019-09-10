pipeline {
    agent wind-node

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven3.6.1') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven3.5.0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('install Stage') {
            steps {
                withMaven(maven : 'maven3.3.1') {
                    sh 'mvn install'
                }
            }
        }
    }
}
