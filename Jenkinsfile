library 'DSL-Library'

pipelineMaven {
  // Configure pipeline options
  def config = [
    branch: 'main',
    repository: 'https://github.com/kappel420/spring-petclinic.git',
    skipTests: true,
    skipInstall: true
  ]
  
  // Call the pipelineMaven script with the config map argument
  call(config) {
    // Pipeline steps...
  }
}
