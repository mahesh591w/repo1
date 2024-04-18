pipeline{

		agent {
				label {
						label "built-in"
						customWorkspace "/mnt/project/"
				}
		
		}
		stages {
		
				stage ('stage4') {
				
							steps {
						
								sh "rm -rf *"
								sh "sudo git clone -b 24Q3 https://github.com/mahesh591w/repo1.git"
								sh "sudo docker cp /mnt/project/repo1/index.html 24Q3://usr/local/apache2/htdocs/"
								
						}
				}
				stage ('stage5') {
				
							steps {
						
								sh "chmod -R 777 /var/lib/docker/volumes/test3/_data/"
						}
				}
		
			
		}

}
