pipeline {
    agent any

    stages {
        stage('Unzip Talend Job') {
            steps {
                bat 'powershell -Command "Expand-Archive -Path job32_0.1.zip -DestinationPath job32 -Force"'
            }
        }

        stage('Run Talend Job') {
            steps {
                bat 'cd job32 && job32_run.bat'
            }
        }
    }
}
