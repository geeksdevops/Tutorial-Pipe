#!groovy
@Library('GlobaLPipeline@master') _
node {
    properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '2', numToKeepStr: '2'))])
    Pipeline_as_code {
        GIT_URL                 = 'https://github.com/pramodvishwa/Tutorial-Pipe.git'
        GIT_CREDENTIALS         = 'Git-Credentials'
	MAVEN_HOME		= '/app/apache-maven/'
        MAVEN_GOAL		= 'clean install'
	SONAR_PROPERTY		= 'sonar-project.properties'
        RECIPIENT               = 'pramod.s.02@gmail.com'
        EMAIL_TEMPLATE          = 'email_template'
    }
}

