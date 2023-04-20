pipeline {
    agent any

    stages {
       
        stage('DOWNLOAD FROM GITHUB') {
            steps {
                git 'https://github.com/gauravrhcss/Green.git'
            }
        }
         stage('REMOTE COPY to system') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: 'JENKINS', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'rsync -e "ssh -p 225"  /var/lib/jenkins/workspace/DON/index.html root@101.53.148.193:/var/www/html', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}
