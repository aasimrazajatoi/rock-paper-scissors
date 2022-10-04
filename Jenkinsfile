pipeline {
    agent any
    stages {   
//         stage ('Source') {
//             steps {
//                 sh 'git clone https://github.com/aasimrazajatoi/rock-paper-scissors.git'                 
                
//             }
//         }
        stage ('build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage ('test') {
            steps {
                echo 'testing'
            }
        }

        stage ('deploy') {
	        steps {
		     sh 'chmod 777 ${WORKSPACE}/target/roshambo-1.0-SNAPSHOT.jar'
		     sh	'java -jar ${WORKSPACE}/target/roshambo-1.0-SNAPSHOT' 	 
		 }
         }
   }
}
