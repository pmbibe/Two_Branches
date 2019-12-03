pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000'
        }
    }
    environment {
        CI = 'true'
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
}
