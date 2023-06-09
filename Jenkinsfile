library 'DSL-Library'

agent any

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
                repository: 'https://github.com/kappel420/spring-petclinic.git',
                branch: 'main',
                skipTests: true
            ])
        }
    }
}
