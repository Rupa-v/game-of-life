pipeline { 
    agent {lable 'JDK-MAVEN'}
     stages {
        stage('vcs') {  
            steps {
                git url: 'https://github.com/wakaleo/game-of-life.git',
                 branch: 'declarative'
            }   
        }
        stage('package') {
            steps {
                sh """
                    export PATH=/usr/lib/jvm/java-1.8.0-openjdk-amd64/bin:$PATH
                    mvn package
                  """
            }
        }
    }
}
