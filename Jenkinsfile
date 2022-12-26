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
            sh '''cd /home/ubuntu/workspace/_playbook-_install_awscli_master/
ansible-playbook -i inventories/hosts playbook.yml --tags "tag2"
'''
          }
        }

      }
    }

  }
}