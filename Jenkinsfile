@Library('DSL-Library') _

pipeline {
    agent none
    stages {
        stage('Example') {
            agent {
                label 'tomek'
            }
            steps {
                script {
                    echo "test"
                }
                pipelineMaven([
                    repository: 'https://github.com/kappel420/spring-petclinic',
                    branch: 'main',
                    skipTests: true
                ])
            }
        }
    }
}