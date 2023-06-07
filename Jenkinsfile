library 'DSL-Library'

pipeline {
    agent none
    stages {
        stage ('Example') {
            agent {label 'tomek'}
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