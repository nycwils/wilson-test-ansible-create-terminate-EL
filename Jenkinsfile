node('master') {
    def app



    stage("Clone repository") {
        checkout scm
        }



    stage("Run Ancible Playbook") {

        
            withCredentials([file(credentialsId: '92045f3a-fdb3-491e-ad2e-d6b9fe7aa3e5', variable: 'mySecretKey')]){

            sh "pwd"
            sh "pwd"
            sh "ls"
            
            //sh "rm Wilson-Test-EC2KeyPair.pem"
            sh "chmod -R 777 /var/lib/jenkins/workspace/wilson-test-ansible-create-terminate-EL"
            sh "cp \$mySecretKey /var/lib/jenkins/workspace/wilson-test-ansible-create-terminate-EL"
            sh "ls"
            //sh "chmod 0400 Wilson-Test-EC2KeyPair.pem"
            sh "chmod 0400 Wilson-Test-EC2KeyPair.pem"
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
