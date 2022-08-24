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
		id
		source ~/.bashrc
    cd ${WORKSPACE}/hello_world
    mvn install
    '''
		}
	}
	stage('mvn deploy'){
	    steps {
		    sh '''
		    id
		    source ~/.bashrc
        cd ${WORKSPACE}/hello_world
        mvn deploy
        '''
	   }
	  }
  }
}
