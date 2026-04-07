pipeline {
    agent any

    tools {
        jdk 'Java'
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/yashiz4u-lgtm/jenkins-lab.git'
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
