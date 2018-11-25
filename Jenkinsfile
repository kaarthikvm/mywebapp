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
                     echo "PATH = ${PATH}"'
                     echo "M2_HOME = ${M2_HOME}"
                   '''
            }
        }
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
