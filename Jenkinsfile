pipeline {
  agent any
  stages {
    stage('install apache') {
      parallel {
        stage('install apache') {
          steps {
            sh 'git clone https://github.com/MeghanaMahale/Ansible_playbook-_install_awscli.git'
          }
        }

        stage('yaml') {
          steps {
            readYaml(file: 'playbook.yml', text: 'name: Check for Python')
          }
        }

      }
    }

  }
}