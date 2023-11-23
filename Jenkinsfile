pipeline {
    agent any // the code will run on any jenkins node or you can specifiy the node name

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "mymaven"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/Sumit900/devopscode.git'

                // Run Maven on a Unix agent.
                sh "mvn clean install"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}
