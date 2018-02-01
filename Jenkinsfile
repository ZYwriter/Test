pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -v '
      }
    }
    stage('Test') {
      steps {
        emailext(subject: '${currentBuild.result}: ${env.JOB_NAME} [${env.BUILD_NUMBER}]', to: '$class: FirstFailingBuildSuspectsRecipientProvider', from: '790333234@qq.com', compressLog: true, attachLog: true, body: '" "')
      }
    }
  }
}