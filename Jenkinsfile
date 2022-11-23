pipeline{

agent {

	label{
			label "built-in"
			customWorkspace "/var/www/html"
	}
}

stages {

	stage('install')

	{
		steps {
				sh "rm -rf *"
				sh "yum install httpd -y"
			}
	}





	stage('httpd-start')

	{
	
	
	
		steps {

				sh "service httpd start"
				echo "Hellow All" >> /var/www/html/index.html
				
				 
				sh "chmod -R 777 index.html"
			}
	}


}



}
