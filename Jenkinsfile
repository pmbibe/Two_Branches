pipeline {
  agent any
  if (${BRANCH_NAME} == "master"){
      stages {
        stage('Prepare') {
          steps {
            echo "--------------------Prepare Stage---------------------"
            echo "${BRANCH_NAME}"
          }
        }
      }
  }
}
