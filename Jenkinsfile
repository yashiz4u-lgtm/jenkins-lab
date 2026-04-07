pipeline {
    agent any

    tools {
        jdk 'Java'
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/yashiz4u-lgtm/jenkins-lab.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
