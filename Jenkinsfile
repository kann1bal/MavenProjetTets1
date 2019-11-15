pipeline {

    agent {

        label "master"
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

        stage ('Initialize') {
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

                   "mvn clean"

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
