pipeline {
    agent any

    stages {
        stage('Get Latest Sourcecode') {
            steps {
	        git 'https://github.com/gautham-kukutla/Jenkins_multijob_pipeline_code.git'
            }
        }
        stage('Compile') {
            steps {
		    withMaven(maven : 'apache-maven-3.8.4'){
                 	bat "mvn clean compile"
		  }}
        }
        stage('Test') {
            steps {
		    withMaven(maven : 'apache-maven-3.8.4'){
			input message: 'Are you sure to proceed to next step? ', ok: 'Yes'
              		 bat "mvn test"
		    }
            }
        }
    }
}
