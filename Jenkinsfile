pipeline {
    agent any

    stages {
        stage('pull code') {
            steps {
                //git credentialsId: 'gin-test-jenkins', url: 'https://github.com/qq23001186/gin_test.git'
            }
        }
        stage('build project') {
            steps {
                sh '''echo “开始构建”
                        echo “构建完成”'''
            }
        }
        stage('deploy project') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: '192.168.124.51', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'echo “jenkins test success”', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: 'gin_test', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'target/**')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}
