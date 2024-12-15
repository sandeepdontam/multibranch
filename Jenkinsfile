pipeline
{
    agent any
    stages
    {
        stage ('continuous download master')
        {
            steps
            {
                git branch: 'main', url: 'https://github.com/sandeepdontam/devops_training.git'
            }
        }
        stage (' continuous build master')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage ('continuous delivery master')
        {
            steps
            {
                deploy adapters: [tomcat9(credentialsId: 'af5b9d7c-fe5c-4dd3-8355-cdd7b7d462d0', path: '', url: 'http://3.23.92.104:8080/')], contextPath: 'sandeepdemo', war: '**\\*.war'
            }
        }
    }
}
