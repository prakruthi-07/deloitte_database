pipeline{
    agent any

    tools
    {
        maven 'maven'
    }
    stages {
        stage('source from git')
        {
            steps{
                git branch: 'main', url: 'https://github.com/prakruthi-07/jenkins.git'
            }
        }
        stage('clean'){
            steps{
                sh 'mvn clean'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
