pipeline{
agent any
stages{
stage('master'){
steps{
		sh 'cp -r index.html /var/www/html'
		sh 'chmod -R 777 /var/www/html/index.html'
}
}
stage('dev'){
steps{
		sh 'cp -r dev.html /var/www/html'
		sh 'chmod -R 777 /var/www/html/dev.html'
}
}
stage('qa'){
steps{
		sh 'cp -r qa.html /var/www/html'
		sh 'chmod -R 777 /var/www/html/qa.html'
}
}
stage('restart-httpd'){
steps{
		sh 'systemctl restart httpd'
		
}	
}
	stage('install-tree'){
steps{
		sh 'yum remove tree -y'
		
}
}
}
}
