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

        NENEXUS_URL = "localhost:8081"

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

        

        stage("mvn clean install ") {

            steps {

                script {

                    // If you are using Windows then you should use "bat" step

                    // Since unit testing is out of the scope we skip them

                    mvn clean

                }

            }

        }

        stage("mvn test ") {

            steps {

                script {

                    // If you are using Windows then you should use "bat" step

                    // Since unit testing is out of the scope we skip them

                    bat "mvn test"

                }

            }

        }

     

    

        

       

}





}
