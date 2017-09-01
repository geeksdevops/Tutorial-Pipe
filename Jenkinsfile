pipeline {
    agent {
	label "linux"
    }
    tools {
        maven 'MAVEN'
        jdk 'JAVA'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = %PATH%"
                '''
            }
        }

        stage ('Build') {
            steps {
		sh '''
                    cd NumberGenerator && mvn install
		   '''
            }
             post {
                success {
                    junit 'NumberGenerator/target/surefire-reports/*.xml'
                        }
                 }
               

           
            }
        }
    
}
