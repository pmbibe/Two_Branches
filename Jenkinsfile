pipeline {
    agent any
        stages{
            stage('Hello') {
                steps {
                    checkout([$class: 'GitSCM', branches: [[name: '**']], browser: [$class: 'GithubWeb', repoUrl: 'https://github.com/pmbibe/Two_Branches'], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'CleanBeforeCheckout']], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'pmbibe', url: 'https://github.com/pmbibe/Two_Branches']]])
                }
            }
            stage('Deliver for development') {
                when {
                    branch 'master'
                }
                steps {
                    echo "${BRANCH_NAME}"
                    input message: 'Finished using the web site? (Click "Proceed" to continue)'
               }
         }
         stage('Deploy for production') {
             when {
                 branch 'slave'
             }
             steps {
                 echo "${BRANCH_NAME}"
                 input message: 'Finished using the web site? (Click "Proceed" to continue)'
             }
         }
        }
}

