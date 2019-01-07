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
                     whoami
                     ls /home/ec2-user/apache-maven-3.5.4                     
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
        
        stage ('Deloyment Stage') {

            steps {
                //withMaven(maven : 'KaarthikMaven') {
                    echo "deloyment"
                    sh '''
                        ls /home/
                        scp  -o StrictHostKeyChecking=no -i /home/ec2-user/KaaSSHKey.pem target/*.war ubuntu@ec2-3-17-59-45.us-east-2.compute.amazonaws.com:/opt/tomcat/webapps/.
                        '''
                //}
            }
        }

    }
}
