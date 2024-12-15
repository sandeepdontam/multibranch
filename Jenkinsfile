pipeline
{
    agent any
    stages
    {
        stage ('continuous download bank_branch')
        {
            steps
            {
                git branch: 'main', url: 'https://github.com/sandeepdontam/devops_training.git'
            }
        }
        stage (' continuous build bank_branch')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        }
    }
