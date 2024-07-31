pipeline {
    agent any
    # agent {
    #    label 'ja01'  // Specify the agent by its label or name
    # }
    
    stages {
        stage('Check AWS CLI Version') {
            steps {
                script {
                    // Execute the AWS CLI version command and capture the output
                    def awsVersion = sh(script: 'aws --version', returnStdout: true).trim()
                    
                    // Print the AWS CLI version to the Jenkins log
                    echo "AWS CLI Version: ${awsVersion}"
                }
            }
        }
    }
    
    post {
        always {
            // Actions that are always performed after the pipeline execution
            echo 'Pipeline execution completed.'
        }
    }
}
