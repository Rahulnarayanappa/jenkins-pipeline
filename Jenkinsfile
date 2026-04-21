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
                 agent { label 'rhel-worker' }
        steps {
          echo "this is deploy stage"
        }
      }
       stage ('Test'){
         agent { label 'master' }
        steps {
          echo "this is test stage"
        }
      }
  }
}
