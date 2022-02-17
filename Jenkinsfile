pipeline {
    agent any
    environment{
      GIT_COMMIT_USER = ''
    }
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
            when{
                expression{
                      GIT_COMMIT_USER != 'sampathkaran'
                   }
                }
            steps {
                echo "hey ${GIT_COMMIT_USER}"
            }  
        }
      }

        
    }
 
