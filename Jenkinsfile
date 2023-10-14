node {
    def customImage = 'node:16-buster-slim'

    
    docker.image(customImage).withRun('-p 3000:3000') {
        // Tahap 'Build'
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
