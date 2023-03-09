pipeline { 
    agent { lable 'JDK-MAVEN' }
     stages {
        stage ('vcs') {  
            steps {
                git url: 'https://github.com/Rupa-v/game-of-life.git',
                branch: 'master'
            }   
        }
        stage ('package') {
            steps {
                sh """
                      export PATH=/usr/lib/jvm/java-1.8.0-openjdk-amd64/bin:$PATH
                      mvn package
                   """
            }
        }
    }
}

