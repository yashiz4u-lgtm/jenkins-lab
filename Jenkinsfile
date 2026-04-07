pipeline {
    agent any

    tools {
        jdk 'Java'
        maven 'Maven'
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/yashiz4u-lgtm/jenkins-lab.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
}
