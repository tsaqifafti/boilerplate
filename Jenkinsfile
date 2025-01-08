// pipeline laravel boiler plate

pipeline {
	agent any
	environment {
			TARGET_DIR = "C:\\Users\\Administrator\\Downloads\\laravel-boilerplate"
	}
	stages {
		stage('Build laravel with composer'){
			steps {
				bat 'composer install'
			}
		}
		stage('Build & Scan'){
		steps {
				echo "Build Project Maven & Scan with scancentral SAST"

				dir ("${TARGET_DIR}") {
//					bat 'scancentral -url http://192.168.1.186:8080/scancentral-ctrl start -bt mvn -upload -versionid 10002 -uptoken f2a08e91-3e45-4d1f-963a-0efde16f1a31'
					bat 'scancentral -url http://192.168.1.186:8080/scancentral-ctrl start'
				}
			}
		}
	}	
}