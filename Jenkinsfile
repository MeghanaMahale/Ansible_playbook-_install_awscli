pipeline {
  agent any
  stages {
    stage('install apache') {
      parallel {
        stage('install apache') {
          steps {
            sh 'echo "hello"'
          }
        }

        stage('yaml') {
          steps {
            readYaml(file: 'playbook.yml', text: '- name: Check for Python')
          }
        }

        stage('') {
          steps {
            sh ' ansible-playbook -i --tags=tag1 playbook.yml'
          }
        }

      }
    }

  }
}