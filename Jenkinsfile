// Pipeline para proyectos Android
//
// V.1.0.0
//

def server_up = false

pipeline {
	agent any
   // agent { label "win" }
    stages {
        stage('Build') {
            steps {
		sh "./gradlew assembleDebug"
            }
        }
	stage('Compile') {
	    steps {
            archiveArtifacts artifacts: '**/*.apk', fingerprint: true, onlyIfSuccessful: true            
	    }
	}
	    
	
    }
}
    
