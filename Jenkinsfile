pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                //withMaven(maven : 'KaarthikMaven') {
                    //sh 'mvn clean compile'
                    echo "compilation"
                
                //}
            }
        }

        stage ('Testing Stage') {

            steps {
                //withMaven(maven : 'KaarthikMaven') {
                    //sh 'mvn test'
                    echo "testing"
                //}
            }
        }


        stage ('Packaging Stage') {
            steps {
                //withMaven(maven : 'KaarthikMaven') {
                    //sh 'mvn package'
                    echo "packaging"
                //}
            }
        }
    }
}
