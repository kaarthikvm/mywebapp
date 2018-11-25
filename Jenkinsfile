pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'KaarthikMaven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'KaarthikMaven') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Packaging Stage') {
            steps {
                withMaven(maven : 'KaarthikMaven') {
                    sh 'mvn package'
                }
            }
        }
    }
}
