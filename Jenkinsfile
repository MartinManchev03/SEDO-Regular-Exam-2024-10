pipeline {
    agent any
  
    stages {
        stage('Restore Dependencies') {
            steps {
                script {
                    sh 'dotnet restore'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'dotnet build --no-restore'
                }
            }
        }

        stage('Run Integration Tests') {
            steps {
                script {
                    sh 'dotnet test --no-build --verbosity normal'
                }
            }
        }
    }
}
