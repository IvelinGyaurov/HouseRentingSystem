
pipeline {
    agent any

    stages {
        stage('Restore') {
            steps {
                bat 'dotnet restore HouseRentingSystem.sln'
            }
        }

        stage('Build') {
            steps {
                bat 'dotnet build HouseRentingSystem.sln --configuration Release --no-restore'
            }
        }

        stage('Test') {
            steps {
                bat 'dotnet test HouseRentingSystem.sln --configuration Release --no-build'
            }
        }
    }
}
