pipeline {

    agent {

        label "master"
    }
    
    tools { 
        maven 'Maven 3.3.9' 
        jdk 'jdk8' 
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
               
            }
        }

        stage("mvn clean install ") {

            steps {

                script {

                    // If you are using Windows then you should use "bat" step

                    // Since unit testing is out of the scope we skip them

                   bat "mvn clean"

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
