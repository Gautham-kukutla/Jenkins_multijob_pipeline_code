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
                 	sh "mvn clean compile"
		  }
        }
        stage('Test') {
            steps {
              		 sh "mvn test"
		    }
            
        }
    }
}
