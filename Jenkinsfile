node('node1'){
    stage('scm'){
         git 'https://github.com/gmuni/game-of-life.git'
         }
        stage('build') {
                sh script: 'mvn clean package'
        }
        stage('post build') {
                junit 'gameoflife-web/target/surefire-reports/*.xml'
                archiveArtifacts 'gameoflife-web/target/*.war'
            }
        }
