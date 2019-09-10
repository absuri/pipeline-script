pipeline {
    agent wind-node

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'mvn3.6.1') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'mvn3.5.3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('install Stage') {
            steps {
                withMaven(maven : 'mvn3.3.3') {
                    sh 'mvn install'
                }
            }
        }
    }
}
