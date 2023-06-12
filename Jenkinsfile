library 'DSL-Library'

    pipeline {
        agent {
            label 'tomek'
        }
        stages {
            stage('run pipeline') {
                steps{
                pipelineMaven([
                    skipTests: false,
                    skipInstall: false
                    ])
            }
            }
        }
    }
