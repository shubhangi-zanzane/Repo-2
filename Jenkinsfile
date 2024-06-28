pipeline {

    agent any
    stages{
        stage('git')
        {
            steps
            {
            git branch:'2024-Q1', url:'https://github.com/shubhangi-zanzane/Repo-2.git'    
            }
        }
        stage('install')
        {
            steps{
                sh 'docker stop server'
                sh 'docker system prune -a -f'
              
                
             //  sh 'docker exec -it server bash'
                sh 'mkdir -p /usr/local/apache2/htdocs '
                 
               sh 'cp index.html /usr/local/apache2/htdocs '
                
                sh 'chmod -R 777 /usr/local/apache2/htdocs/index.html '
                 sh 'docker run -itdp 80:80 --name server httpd '
                
        }
    }
    }
    

    
}
