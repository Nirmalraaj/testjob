node{
   stage('SCM Checkout'){
     git 'https://github.com/bhavanimahalingam/testjob'
   }
   stage('Deploy to Tomcat'){
      sshagent(['tomcat_jenkins']){
      sh 'scp -o StrictHostKeyChecking=no /home/ec2-user/var/lib/jenkins/workspace/bavani_webapp/target/*.war  ec2-user@3.88.59.170:/apache-tomcat-7.0.104/webapps/'
      }
  }
}
   
  
