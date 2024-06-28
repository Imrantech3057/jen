@Library('mylibrary')_
pipeline
{
    agent any
    stages
    {
        stage('continuous Download')
        {
            steps
            {
                script
                {
                    cicd.gitDownload("jen.git")
                }
            }
        }
        stage('continuous Build')
        {
            steps
            {
                script
                {
                    cicd.mavenBuild()
                }
            }
        }
        stage('continuous Deploy')
        {
            steps
            {
                script
                {
                    cicd.deploy("Testing","172.31.46.229","testapp")
                }
            }
        }
        stage('continuous Test')
        {
            steps
            {
                script
                {
                    cicd.gitDownload("Functionaltesting.git")
                    cicd.runselenium("Testing")
                }
            }
        }
        stage('continuous delivery')
        {
            steps
            {
                script
                {
                    cicd.deploy("Testing","172.31.38.218","prod")
                }
            }
        }
    }
}
