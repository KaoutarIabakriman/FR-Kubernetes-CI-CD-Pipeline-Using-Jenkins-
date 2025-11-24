pipeline {
    agent {
        label "jenkins-agent"
    }

    tools {
        maven 'Maven3'
        jdk "java17"
    }

    stages {
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Checkout from SCM') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/dmancloud/complete-prodcution-e2e-pipeline'
            }
        }

    }
}
