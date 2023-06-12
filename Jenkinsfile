library 'DSL-Library'

    pipeline {
        agent {
            label 'tomek'
        }
        stages {
            stage('run pipeline') {
                steps{
                pipelineMaven([
                    skipTests: 0,
                    skipInstall: 0
                    ])
            }
            }
        }
    }
