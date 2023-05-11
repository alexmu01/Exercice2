pipeline {
  agent any
  stages {
    stage('check-user') {
      steps {
        sh '''id jenkins
if [ $? -eq 1 ] 
then
    echo "user exist"
else
    echo " user not exist"
fi'''
      }
    }

    stage('find_files') {
      steps {
        sh 'sudo find /var/lib -user jenkins '
      }
    }

    stage('list_files') {
      steps {
        sh 'ls -li /jenkins'
      }
    }

  }
}