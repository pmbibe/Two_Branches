pipeline {
    agent any
        stages{
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

