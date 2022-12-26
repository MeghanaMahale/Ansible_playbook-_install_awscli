pipeline {
  agent any
  stages {
    stage('install apache') {
      steps {
        readYaml(file: 'playbook.yml', text: 'Check for Python')
      }
    }

  }
}