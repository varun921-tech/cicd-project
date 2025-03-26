    pipeline {
        agent any
    
        stages {
            stage('Build') {
                steps {
                    git branch: 'dev', credentialsId: '18671910-e369-49dd-a6d6-576c02fa9722', url: 'https://github.com/varun921-tech/cicd-project.git'
                }
            }
            stage('Test'){
                steps {
                    withMaven(maven: 'mymaven'){
                        sh "mvn test"
                    }
                }
            }
            stage('Package'){
                steps {
                    withMaven(maven: 'mymaven'){
                        sh "mvn package"
                    }
                }
            }
            // stage('Results'){
            //     steps {
            //         junit '**/*.xml'
            //         archiveArtifacts artifacts: '**/*.war', followSymlinks: false
                    
                 
            //     }
            // }
            
        }
    }

