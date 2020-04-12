node('master') {
    def app



    stage("Clone repository") {
        checkout scm
        }



    stage("Run Ancible Playbook") {

        
            withCredentials([file(credentialsId: 'wilson-test-pem', variable: 'mySecretKey')]){

            sh "pwd"
            sh "pwd"
            //sh "ls"
            
            //sh "rm Wilson-Test-EC2KeyPair.pem"
            sh "chmod -R 777 /var/lib/jenkins/workspace/wilson-test-pipeline"
            sh "cp \$mySecretKey /var/lib/jenkins/workspace/wilson-test-pipeline"
            sh "ls"
            //sh "chmod 0400 Wilson-Test-EC2KeyPair.pem"
            sh "chmod 0400 wilson-test-sps-keypair.pem"
            sh "python --version"
            sh "pip --version"
            sh "pip install --user boto"
            sh "pip install --user boto3"
            
            sh "ansible-playbook playbook.yaml -vvv -i inventory.txt"




            }
          
        }

 

  
    stage("Wipe Out Jenkins Temp Workspace") {

      deleteDir()
       
    }

}
