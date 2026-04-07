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
                sh 'echo Building with Maven...'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Running tests...'
            }
        }
    }
}
