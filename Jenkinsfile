library 'DSL-Library'
//@Library('DSL-Library') _

pipeline {
    // repository: 'https://github.com/kappel420/spring-petclinic', branch: 'main', skipTests: true
    agent none
    stages {
        stage ('Example') {
            agent {label 'tomek'}
            steps {
                // log.info 'Starting' 
                script { 
                    echo "test"
                }
                //pipelineMaven([repository: 'https://github.com/kappel420/spring-petclinic', branch: 'main', skipTests: false])
                //pipelineMaven()
                pipelineMaven(repository: 'https://github.com/kappel420/spring-petclinic', branch: 'main', skipTests: true)
            }
        }
    }
}