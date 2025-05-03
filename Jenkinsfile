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
                git branch: 'master', url:'https://github.com/prakruthi-07/deloitte_database.git'
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
