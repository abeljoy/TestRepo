pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/kishorekk12/pipelineTest.git', branch: 'master', poll: true)
      }
    }

    stage('Compile') {
      steps {
        bat 'mvn compile'
      }
    }

    stage('Archieve') {
      steps {
        archiveArtifacts(artifacts: '**/*.class', onlyIfSuccessful: true)
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployed'
      }
    }

  }
}