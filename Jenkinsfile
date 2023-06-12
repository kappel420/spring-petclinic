library 'DSL-Library'

    pipeline {
        agent {
            label 'tomek'
        }
        stages {
            stage('run pipeline') {
                pipelineMaven([
                    repository: 'https://github.com/kappel420/spring-petclinic.git',
                    branch: 'main',
                    skipTests: true,
                    skipInstall: true
                    ])
            }
        }
    }
