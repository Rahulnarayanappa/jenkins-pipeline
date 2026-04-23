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
       stage('Test') {
	parallel {
		stage('Test1') {
			steps {
				echo "this is test1"
			}
		}
		stage ('Test2') {
			steps {
				echo "this is test2"
			}
		}
	}
         agent { label 'master' }
        steps {
          echo "this is test stage"
        }
      }
  }
}
