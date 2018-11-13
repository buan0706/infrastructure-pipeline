
properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/buan0706/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
}





