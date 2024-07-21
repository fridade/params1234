pipeline {
    agent any
    parameters {
      string description: 'Please Enter your firstname', name: 'firstName'
      string description: 'Please Enter your lastname', name: 'lastName'
    }


    stages {
        stage('welcome stage') {
            steps {
                echo "hi ${params.firstName} ${params.lastName}, welcome"
            }
        }
    }
}
