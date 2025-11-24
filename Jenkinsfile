pipeline(
    agent{
        label "jenin-agent"
    }

    tools {
        maven "Maven3"
        jdk "java17"
    }

    stages {
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
            }
        }
    }

    stages {
        stage('Checkout from SCM') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/dmancloud/complete-prodcution-e2e-pipeline'
            }
        }
    }
)