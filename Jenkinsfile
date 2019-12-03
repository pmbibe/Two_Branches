pipeline {
    agent any
        stages{
            stage('Hello') {
                checkout([$class: 'GitSCM', branches: [[name: '**']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'CleanCheckout']], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'pmbibe', url: 'https://github.com/pmbibe/Two_Branches']]])
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

