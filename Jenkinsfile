pipeline {
    agent {
      node { label 'workstation' }
    }

    stages {

      stage ('Build') {
        steps {
          sh 'npm install'
        }
      }

      stage ('Unit-Tests') {
        steps {
          echo 'Unit-Tests'
          //sh 'npm test'
        }
      }

      stage ('Code-Analysis') {
        steps {
          sh 'sonar-scanner -Dsonar.host.url=http://172.31.92.0:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=catalogue'
        }
      }

      stage ('Security Checks') {
        steps {
          echo 'Security Checks'
        }
      }

      stage ('Publish Artifact') {
        steps {
          echo 'Publish Artifact'
        }
      }
    }
}