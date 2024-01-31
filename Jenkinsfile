pipeline{
    agent any
    stages{
        stage("Test"){
            steps{
                sh """
                       echo "Welcome to Jenkins Sijuade"
                   """    
            }
        }
        stage("Deploy Upadte3"){
            steps{
                sh """
                       echo "Welcome to the Deploynent. Added Jenkins"
                       ssh -o StrictHostKeyChecking=no -T -i /var/lib/jenkins/user-key.pem ubuntu@ec2-44-211-31-44.compute-1.amazonaws.com
                       sudo apt update -y
                       cd /var/www
                       sudo rm -rf html
                       git clone https://github.com/syjjem/jenk.git html
                   """    
            }
        }
    }
}