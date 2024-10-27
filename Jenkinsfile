pipeline {
    agent any
    stages {
        stage('Restore dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Dotnet Build') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Execute Unit and Integration tests') {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
