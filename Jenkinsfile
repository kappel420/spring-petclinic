library 'DSL-Library'

pipeline {
    agent none
    stages {
        stage ('Example') {
            agent agent
            steps {
                // log.info 'Starting' 
                script { 
                    log.info 'Starting'
                    log.warning 'Nothing to do!'
                }
            }
        }
    }
}