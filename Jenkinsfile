pipeline {
    agent any
    triggers {
        pollSCM('5 * * * *')
    }
    tools {
        maven 'maven3.9.9'
        jdk 'java17'
    }
    stages {
        stage('SCM') {
            steps {
                git url: 'https://github.com/Bhavish3000/game-of-life_fork.git',
                    branch: 'master'
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean package'
            }
        }

    }
}