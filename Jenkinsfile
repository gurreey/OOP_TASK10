pipeline {
    agent any

    environment {
        SONAR_SCANNER_HOME = 'C:\\sonar-scanner-5.0.1.3006-windows\\bin'
        SONAR_HOST_URL = 'http://localhost:9000'
        SONAR_PROJECT_KEY = 'Zaki_Daahir'
        SONAR_LOGIN = 'sqa_bef6f70347d33963bc7c85fb3700ae27cef65517'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/gurreey/Jenkins.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('TASK9') {
                   bat 'C:\\sonar-scanner-5.0.1.3006-windows\\bin\\sonar-scanner -Dsonar.projectKey=Zaki_Daahir -Dsonar.sources=src -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqa_bef6f70347d33963bc7c85fb3700ae27cef65517'
                }
            }
        }
    }
}
