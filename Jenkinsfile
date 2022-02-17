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
                    GIT_COMMIT_USER = sh (
                        script: 'git --no-pager show -s --format=\'%an\'',
                        returnStdout: true
                    ).trim()
                    echo "Git committer email: ${GIT_COMMIT_USER}"
                   }
                 }
                }
            }
        stage('print message'){
            steps {
                echo "hey ${GIT_COMMIT_USER}"
            }  
        }
      }

        
    }
 
