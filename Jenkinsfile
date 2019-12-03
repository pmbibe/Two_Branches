pipeline {
    agent {
       any
    }
   

        stage('Deliver for development') {
            when {
                branch 'development'
            }
            steps {
                echo "${BRANCH_NAME}"
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'
            }
            steps {
                echo "${BRANCH_NAME}"
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
            }
        }
}
