pipeline {
  agent {
    node {
      label 'ansible'
    }

  }
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

        stage('error') {
          agent {
            node {
              label 'ansible'
            }

          }
          steps {
            sh '''ansible-playbook -i inventories/hosts playbook.yml --tags "tag1"

'''
          }
        }

        stage('tag2') {
          agent {
            node {
              label 'ansible'
            }

          }
          steps {
            sh '''ansible-playbook -i inventories/hosts playbook.yml --tags "tag2"
'''
          }
        }

      }
    }

  }
}