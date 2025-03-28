    pipeline {
        agent any
    
        stages {
            stage('Build') {
                steps {
                    git branch: 'dev', credentialsId: 'f4708822-3927-49ed-a7c7-99f3573cb18f', url: 'https://github.com/varun921-tech/cicd-project.git'
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

