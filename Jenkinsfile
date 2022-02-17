pipeline {

    environment {
        AGENT_INFO = ''
    }

    agent any
    stages {

        stage('Collect agent info'){
            steps {
                 dir("${WORKSPACE}/code"){
                 script {
                    GIT_COMMIT_EMAIL = sh (
                        script: 'git --no-pager show -s --format=\'%an\'',
                        returnStdout: true
                    ).trim()
                    echo "Git committer email: ${GIT_COMMIT_EMAIL}"
                   }
                 }
                }
            }
        }

        
    }
 
