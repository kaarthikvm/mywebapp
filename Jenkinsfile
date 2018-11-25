pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                //withMaven(maven : 'KaarthikMaven') {
                    //sh 'mvn clean compile'
                    echo "compilation"
                    sh 'echo "PATH = ${PATH}"'
                    sh 'echo "M2_HOME = ${M2_HOME}"'
                
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
