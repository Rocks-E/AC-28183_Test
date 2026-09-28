// execute this before anything else, including requesting any time on an agent
if (currentBuild.getBuildCauses().toString().contains('BranchIndexingCause')) {
	print "INFO: Build skipped due to trigger being Branch Indexing"
	currentBuild.result = 'ABORTED'
	return
}

pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				error 'AC-28183 notification test'
			}
		}
	}
}