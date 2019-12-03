pipeline {
  agent any

      stages {
          if (${BRANCH_NAME} == "master"){
           stage('Prepare') {
            steps {
              echo "--------------------Prepare Stage---------------------"
              echo "${BRANCH_NAME}"
          }
        }
      }
  }
}
