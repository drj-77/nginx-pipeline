pipeline {
agent any

	stages {
		stage ('install-nginx')
		{
			steps {
				sh 'sudo apt update -y'
				sh 'sudo apt install nginx -y'
			}
		}
		
		stage ('deploy-index')
		{
			steps {
				sh 'sudo echo "Welcome to Young Minds. Keep Learning!! Keep Growing!!" > index.html'
				sh 'sudo mv index.html /var/www/html/index.html'

			}
		}

		stage ('Nginx-stop')
		{
			steps {
				sh 'sudo systemctl stop nginx'
			}
		}

		stage ('Start-nginx')
		{
			steps {
				sh 'sudo systemctl start nginx'
			}
		}
		
	}
}
