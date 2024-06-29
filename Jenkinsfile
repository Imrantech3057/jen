@Library('mylibrary)_
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
                    cicd.gitDownload("jen")
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
    }
}
