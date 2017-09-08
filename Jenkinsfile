 node('master') {
      
    stage ('Git Checkout')
    {
          dir ('vagrant') { 
          git 'https://github.com/harishchanderdalal/bashinhost.git'
    	      echo 'git Clone'
             }
    }
 
    stage ('vagrant box')
    {
          dir ('vagrant') {
          sh 'vagrant box add dummy https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box'
             echo 'Vagrant Ready'
             }
    }
 
    stage ('Ec2 Provison')
    {
       dir ('vagrant') {
       sh 'vagrant up --provider=aws'
             echo 'Ec2 Created'
             } 
            }
  
  }     
             
