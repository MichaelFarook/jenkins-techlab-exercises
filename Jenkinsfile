pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '6'))
        timeout(time: 10, unit: 'MINUTES')
        timestamps()  // Timestamper Plugin
        disableConcurrentBuilds()
    }
    environment {
        GREETING_TO = 'Jenkins Techlab'
    }
    stages {
        stage('Greeting') {
            steps {
                echo "Hello, ${env.GREETING_TO}!"
                
                sh 'echo "Hello, $GREETING_TO!"'
            }
        }
    }
}
