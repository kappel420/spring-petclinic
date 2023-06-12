library 'DSL-Library'

pipelineMaven([
    repository: 'https://github.com/kappel420/spring-petclinic.git',
    branch: 'main',
    skipTests: true,
    skipInstall: true
]) {
    // Pipeline stages go here
    stage('Fetch Source Code') {
        steps {
            checkout([$class: 'GitSCM',
                branches: [[name: params.branch ?: 'main']],
                userRemoteConfigs: [[url: params.repository ?: '']],
                extensions: [[$class: 'CleanBeforeCheckout'], [$class: 'CloneOption', honorRefspec: false]]])
        }
    }
    
    stage('Build') {
        steps {
            sh 'mvn package -DskipTests'
        }
    }
    
    stage('Run Tests') {
        steps {
            script {
                if (!params.skipTests) {
                    sh 'mvn verify'
                    junit '**/target/surefire-reports/*.xml'
                }
            }
        }
    }
    
    stage('Install Artifact') {
        steps {
            script {
                if (!params.skipInstall) {
                    sh 'mvn install -DskipTests'
                }
            }
        }
    }
}