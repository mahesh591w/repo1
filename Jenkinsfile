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
						
								sh "sudo docker volume create test1"
								sh "sudo docker volume create test2"
								sh "sudo docker volume create test3"
								
						}
				}
				stage ('stage1') {
				
							steps {
						
								sh "sudo docker run -itdp 82:80 -v test1:/usr/local/apache2/htdocs/ --name 24Q1 httpd"
								sh "sudo docker run -itdp 83:80 -v test2:/usr/local/apache2/htdocs/ --name 24Q2 httpd"
								sh "sudo docker run -itdp 84:80 -v test3:/usr/local/apache2/htdocs/ --name 24Q3 httpd"
								
						}
				}
				stage ('stage2') {
				
							steps {
						
								sh "rm -rf *"
								sh "git clone -b 24Q1 https://github.com/mahesh591w/repo1.git"
								sh "sudo docker cp /mnt/project/repo1/index.html 24Q1://usr/local/apache2/htdocs/"
								
						}
				}
				stage ('stage3') {
				
							steps {
						
								sh "rm -rf *"
								sh "sudo git clone -b 24Q2 https://github.com/mahesh591w/repo1.git"
								sh "sudo docker cp /mnt/project/repo1/index.html 24Q2://usr/local/apache2/htdocs/"
								
						}
				}
				stage ('stage4') {
				
							steps {
						
								sh "rm -rf *"
								sh "sudo git clone -b 24Q3 https://github.com/mahesh591w/repo1.git"
								sh "sudo docker cp /mnt/project/repo1/index.html 24Q3://usr/local/apache2/htdocs/"
								
						}
				}
		
			
		}

}
