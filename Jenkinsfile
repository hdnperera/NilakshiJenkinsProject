pipeline {
    agent any

    environment {
        GIT_URL = 'https://github.com/hdnperera/NilakshiJenkinsProject.git'
        STAGING_ENV = 'StagingServer'
        PRODUCTION_ENV = 'ProductionServer'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building the code using Maven"
                    echo "Tool: Maven"
                }
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo "Running unit and integration tests"
                    echo "Tools: JUnit, TestNG"
                }
            }
        }

        stage('Code Analysis') {
            steps {
                script {
                    echo "Analyzing the code using SonarQube"
                    echo "Tool: SonarQube"
                }
            }
        }

        stage('Security Scan') {
            steps {
                script {
                    echo "Performing a security scan using OWASP Dependency-Check"
                    echo "Tool: OWASP Dependency-Check"
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                script {
                    echo "Deploying the application to staging environment: ${STAGING_ENV}"
                }
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo "Running integration tests on the staging server"
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                script {
                    echo "Deploying the application to production environment: ${PRODUCTION_ENV}"
                }
            }
        }
    }
}
