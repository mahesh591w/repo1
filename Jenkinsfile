pipeline{

		agent {
				label {
						label "built-in"
						customWorkspace "/mnt/project/"
				}
		
		}
		stages {
		
				stage ('stage3') {
				
							steps {
						
								sh "rm -rf *"
								sh "sudo git clone -b 24Q2 https://github.com/mahesh591w/repo1.git"
								sh "sudo docker cp /mnt/project/repo1/index.html 24Q2://usr/local/apache2/htdocs/"
								
						}
				}
				stage ('stage4') {
				
							steps {
						
								sh "chmod -R 777 /var/lib/docker/volumes/test2/_data/"
								
						}
				}
		
			
		}

}
