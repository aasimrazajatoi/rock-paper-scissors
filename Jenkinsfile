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
                sh 'mvn clean install'
            }
        }

        stage ('test') {
            steps {
                echo 'testing'
            }
        }

        stage ('deploy') {
	        steps {
		     sh	'nohup java -jar ${WORKSPACE}/target/roshambo-1.0-SNAPSHOT' 	 
		 }
         }
   }
}
