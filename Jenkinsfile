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
    cd ${WORKSPACE}/hello_world
    /opt/maven/bin/mvn install
    '''
		}
	}
	stage('mvn deploy'){
	    steps {
		    sh '''
		    id
        cd ${WORKSPACE}/hello_world
        /opt/maven/bin/mvn deploy
        '''
	   }
	  }
  }
}
