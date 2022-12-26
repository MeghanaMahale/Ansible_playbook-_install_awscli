pipeline {
  agent any
  stages {
    stage('install apache') {
      parallel {
        stage('install apache') {
          steps {
            sh 'mvn'
          }
        }

        stage('java verification') {
          steps {
            readYaml(file: 'playbook.yml', text: 'Check for Python')
          }
        }

      }
    }

  }
}