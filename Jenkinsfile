pipeline {
  agent any
  stages {
    stage('Pull') {
      agent {
        dockerfile {
          filename 'somedocker.yml'
        }

      }
      environment {
        key = 'value'
      }
      steps {
        echo 'Fetching Consul Envs'
        sleep 15
        pwd()
      }
    }
    stage('Slack') {
      steps {
        slackSend(message: 'jenkins', channel: 'devops', baseUrl: 'https://acme-incorporated-hq.slack.com/services/hooks/jenkins-ci/', token: '41xd6RtIEssE91TZof2ngR5C')
      }
    }
  }
}