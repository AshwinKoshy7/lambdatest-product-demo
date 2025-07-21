pipeline {
    agent any

    environment {
        LT_USERNAME = 'ashwinkoshy'
        LT_ACCESS_KEY = 'LT_eesHIc2A3kLNR2AKxhut6J4AFOa86jwNjvMAdUCyuFxhorn'
    }

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/AshwinKoshy7/lambdatest-product-demo'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            junit '**/surefire-reports/*.xml'
        }
    }
}
