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
                    echo "JAVA_HOME = %JAVA_HOME%"
		    echo "MAVAN_HOME = %MAVEN_HOME%"
                '''
            }
        }

        stage ('Build') {
            steps {
                    sh 'cd NumberGenerator & mvn install'
            }
             post {
                success {
                    junit 'NumberGenerator/target/surefire-reports/*.xml'
                        }
                 }
               

           
            }
        }
    
}
