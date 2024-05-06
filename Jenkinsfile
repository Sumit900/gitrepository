pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                //git 'https://github.com/Sumit900/gitrepository.git'
                git branch: 'develop', url: 'https://github.com/Sumit900/gitrepository.git'

                // Run Maven on a Unix agent.
                sh 'echo "This is the first step in the pipeline" && git pull'

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            }
        }
    }
