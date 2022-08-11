properties([
    buildDiscarder(logRotator(numToKeepStr: '5'))
])

timestamps() {
    timeout(time: 10, unit: 'MINUTES') {
        node {
            stage('Greeting') {
                withEnv(['GREETINGS_TO=Jenkins TechLab']) {
                    echo "Hello ${GREETINGS_TO} [${env.BUILD_ID}]"
                    //also available as env variable to a process: 
                    sh 'echo "Hello, $GREETINGS_TO [$BUILD_ID"'
                }
            }
        } 
    }
}
