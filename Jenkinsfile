pipeline {
    agent any
  
        stage('Restore Dependencies') {
            steps {
                script {
                    bat 'dotnet restore'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    bat 'dotnet build --no-restore'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    bat 'dotnet test --no-build --verbosity normal'
                }
            }
        }
}
