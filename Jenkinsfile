pipeline {
    agent any  // Chạy trên bất kỳ agent nào có sẵn
    stages {
        stage('Create Index File') {
            steps {
                script {
                    def filePath = "index.html"
                    writeFile file: filePath, text: "<h1>Welcome to Jenkins</h1>"
                    echo "File index.html has been created!"
                }
            }
        }
        stage('Archive File') {
            steps {
                archiveArtifacts artifacts: 'index.html', fingerprint: true
            }
        }
    }
}
