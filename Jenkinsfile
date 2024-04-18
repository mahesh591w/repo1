pipeline{

		agent {
				label {
						label "built-in"
						customWorkspace "/mnt/project/"
				}
		
		}
		stages {
		
				stage ('stage1') {
				
							steps {
						
								sh "rm -rf *"
								sh "sudo git clone -b 24Q1 https://github.com/mahesh591w/repo1.git"
								sh "sudo docker cp /mnt/project/repo1/index.html 24Q1://usr/local/apache2/htdocs/"
								
						}
				}
				stage ('stage2') {
				
							steps {
						
								sh "chmod -R 777 /var/lib/docker/volumes/test1/_data/"
								
						}
				}
		
			
		}

}
