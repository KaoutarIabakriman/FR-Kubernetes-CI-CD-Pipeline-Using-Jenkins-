pipeline {
    agent {
        label "jenkins-agent"
    }

    tools {
        maven 'Maven3'
        jdk "Java17"
    }

    stages {
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Checkout from SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/KaoutarIabakriman/FR-Kubernetes-CI-CD-Pipeline-Using-Jenkins-'
            }
        }

        stage('Build Application') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test Application') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Sonarqube Analysis') {
            steps {
                    sh 'mvn sonar:sonar'
            }
        }

    }
}
