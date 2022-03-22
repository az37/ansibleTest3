pipeline {
  agent any

  stages {
    stage('Hello') {
      steps {
        sh '''
          ansible --version
          ansible-playbook --version
          ansible-galaxy --version
        '''
      }
    }
    
    stage('Ansible') {
      steps {
        ansiblePlaybook credentialsId: '67c2292f-647b-420a-b77e-fa32adf7527b', disableHostKeyChecking: true, installation: 'Ansible EC2', inventory: 'hosts', playbook: 'firstplaybook.yml'
      }
    }
    
  }
}
