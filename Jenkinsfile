pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "mymaven"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/Sumit900/gitrepository.git'

                // Run Maven on a Unix agent.
                sh 'echo "This is the first step in the pipeline code. In the next step the files will be copied from github repository in develop branch."'

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    sh 'git pull'
                }
            }
        }
    }
}
