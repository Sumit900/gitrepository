pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                //git 'https://github.com/Sumit900/gitrepository.git'
                git branch: 'develop', credentialsId: '2d6617f7-bd97-4a54-8ec9-454d1874b8fc', url: 'https://github.com/Sumit900/gitrepository.git'

                // Run Maven on a Unix agent.
                sh 'echo "This is the first step in the pipeline" && git pull'

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            }
        }
    }
