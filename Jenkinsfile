pipeline {

    agent {

        label "master"
    }
     environment {

        // This can be nexus3 or nexus2

        NEXUS_VERSION = "nexus3"

        // This can be http or https

        NEXUS_PROTOCOL = "http"

        // Where your Nexus is running

        NEXUS_URL = "localhost:8081"

        // Repository where we will upload the artifact

        NEXUS_REPOSITORY = "Releases"

        // Jenkins credential id to authenticate to Nexus OSS

        NEXUS_CREDENTIAL_ID = "admin:admin123"

    }

    stages {

        stage("clone code") {

            steps {

                script {

                    // Let's clone the source

                    git 'https://github.com/kann1bal/MavenProjetTets1.git';

                }

            }

        }

        stage ('Initialize 1sdsd23') {
            steps {
                
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                echo "JAVA_HOME = ${JAVA_HOME}"
               
            }
        }

        stage("mvn clean install ") {

            steps {

                script {

                    // If you are using Windows then you should use "bat" step

                    // Since unit testing is out of the scope we skip them

                bat   " mvn clean install"

                }

            }

        }

        stage("mvn test ") {

            steps {

                script {

                    // If you are using Windows then you should use "bat" step

                    // Since unit testing is out of the scope we skip them

                 bat     'mvn test'

                }

            }

        }

      stage("mvn deploy ") {

            steps {

                script {

                    // If you are using Windows then you should use "bat" step

                    // Since unit testing is out of the scope we skip them

                   bat  "C:\\Program Files\\apache-maven-3.6.1\\bin mvn deploy"

                }

            }

        }
stage("mail") {

          steps {

          
mail bcc: '', body: 'hzelloooooo zied', cc: '', from: '', replyTo: '', subject: 'jenkns subject', to: 'zied.ue@gmail.com'
            
          }

        

        }
    

        

       

}





}
