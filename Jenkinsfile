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
                sh 'mvn clean deploy -s Settings.xml'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
