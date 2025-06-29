pipeline {
    agent any

    stages {
        stage('Build and Test') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet restore'
                bat 'dotnet build --no-restore'
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
