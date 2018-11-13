
properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/buan0706/infrastructure-pipeline.git', branch: 'master'
    stage ("GetInstances") {

        sh "aws ec2 describe-instances --region us-east-1"
        
    }

    //stage ("CreateInstance") {
    
        //sh "aws ec2 run-instances --image-id ami-013be31976ca2c322 --count 1 --instance-type t2.micro --key-name mykeypair --security-group-ids sg-35153d79 --subnet-id subnet-eef57389 --region us-east-1"

    //}
    
    stage ("TerminateInstance") {
    
        sh 'aws ec2 describe-instances --region us-east-1 --filters "Name=instance-type,Values=t2.micro"'
        
    }
}
