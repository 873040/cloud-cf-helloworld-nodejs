  
@Library('piper-lib-os') _
node() {
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }
}
stage('build') {
    mtaBuild script: this
   steps {
                echo 'Building..'
            }
}
  stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
stage('deploy') {
    cloudFoundryDeploy script: this
   steps {
                echo 'Deploying..'
            }
}
