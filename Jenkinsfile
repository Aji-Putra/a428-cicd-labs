node {
    def customImage = 'node:16-buster-slim'

    // Definisikan agent (agen) dalam blok node
    docker.image(customImage).withRun('-p 3000:3000') {
        // Tahap 'Build'
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        // Tahap 'Test'
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
