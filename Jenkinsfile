pipeline {
    agent any
    parameters {
      string description: 'Please Enter your firstname', name: 'firstName'
      string description: 'Please Enter your lastname', name: 'lastName'
      choice choices: ['dev', 'uat', 'prod'], description: 'choose the environment you want to deploy to ', name: 'Environment'
    }


    stages {
        stage('welcome stage') {
            steps {
                echo "hi ${params.firstName} ${params.lastName}, welcome"
            }
        }
        stage('deploy to deve ') {
            when {
              expression {
               params.Environment == "dev"
              }
            }
            steps {
                echo "deploying to dev"
            }
        }
        stage('deploy to UAT ') {
            when {
              expression {
               params.Environment == "uat"
              }
            }
            steps {
                echo "deploying to UAT"
            }
        }
        stage('deploy to prod ') {
            when {
              expression {
               params.Environment == "prod"
              }
            }
            steps {
                echo "deploying to prod"
            }
        }
    }
}
