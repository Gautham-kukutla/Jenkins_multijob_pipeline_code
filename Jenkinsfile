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
		    
                 	bat "mvn clean compile"
		  }
        }
        stage('Test') {
            steps {
              		 bat "mvn test"
		    }
            
        }
    }
}
