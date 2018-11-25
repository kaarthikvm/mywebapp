pipeline {
    agent any
    tools { 
        maven 'KaarthikMaven' 
        //jdk 'jdk8' 
    }
    stages {
        stage ('Initialisation Stage') {
            steps {
                sh '''
                     echo "PATH = ${PATH}"
                     echo "M2_HOME = ${M2_HOME}"
                   '''
            }
        }
        stage ('Compile Stage') {

            steps {
                //withMaven(maven : 'KaarthikMaven') {
                    echo "compilation"
                    sh 'mvn clean compile'
                //}
            }
        }

        stage ('Testing Stage') {

            steps {
                //withMaven(maven : 'KaarthikMaven') {
                    echo "testing"
                    sh 'mvn test'
                //}
            }
        }


        stage ('Packaging Stage') {
            steps {
                //withMaven(maven : 'KaarthikMaven') {
                    echo "packaging"
                    sh 'mvn package'
               //}
            }
        }
    }
}
