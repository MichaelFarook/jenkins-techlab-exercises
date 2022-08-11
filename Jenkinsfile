pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '6'))
        timeout(time: 10, unit: 'MINUTES')
        timestamps()  // Timestamper Plugin
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'Greetings_to', defaultValue: 'Jenkins Techlabs', description: 'Who to greet?')
    }
    stages {
        stage('Greeting') {
            steps {
                echo "Hello, ${params.Greetings_to}!"
            }
        }
    }
}
