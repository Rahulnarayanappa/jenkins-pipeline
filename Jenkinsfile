pipeline {
  agent none
    stages{ 
      stage ('Build'){
        agent { label 'rhel-slave'}
        steps {
          echo "this is build stage"
        }
      }
       stage ('Deploy'){
        steps {
          echo "this is deploy stage"
        }
      }
       stage ('Test'){
        steps {
          echo "this is test stage"
        }
      }
  }
}
