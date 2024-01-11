pipeline {
    agent any

    stages {
        stage('BuildTest') {
            steps {
            git 'https://github.com/shivamrnc/NewTestJenkinsFile.git'
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
            bat 'mvn compile'
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
            bat 'mvn test -Dbrowser = localchrome'
                echo 'Deploying....'
            }
        }
    }
}