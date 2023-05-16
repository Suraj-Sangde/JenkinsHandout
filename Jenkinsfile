pipeline{
agent any
stages{
stage('master'){
steps{
		sh 'cp -r index.html /var/www/html'
		sh 'chmod 777 /var/www/html/index.html'
}
}
stage('dev'){
steps{
		sh 'cp -r dev.html /var/www/html'
		sh 'chmod 777 /var/www/html/index.html'
}
}
stage('qa'){
steps{
		sh 'cp -r qa.html /var/www/html'
		sh 'chmod 777 /var/www/html/index.html'
}
}
stage('restart-httpd'){
steps{
		sh 'systemctl restart httpd'
		
}	
}
