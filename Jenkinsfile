pipeline {
    agent {
        node {
            label 'slave02'
        }
    }
    stages {
	    stage('checkout'){
		    steps{
		    checkout scm
		    }
	    }
	stage('mvn build'){
	    steps {
		sh '''
		source ~/.bashrc
    cd ${WORKSPACE}/hello_world
    mvn install
    '''
		}
	}
	stage('mvn deploy'){
	    steps {
		    sh '''
		    source ~/.bashrc
        cd ${WORKSPACE}/hello_world
        mvn deploy
        '''
	   }
	  }
  }
}
