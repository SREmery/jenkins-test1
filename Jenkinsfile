        pipeline{
            agent any
            stages{
            stage('clean-up'){
            steps{
                    sh "docker rm -f $(docker ps -aq) || true"
                    }
                    }
            stage('build'){
            steps{
                     sh "docker build -t ."
                    }
            }
            stage('run'){
            steps{
                     sh "docker run -d -p 80:5500 jenkins jenkinsimage"
                }
            }
        }
    }
