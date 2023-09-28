        pipeline{
            agent any
            stages{
            stage('clean-up'){
            steps{
                    sh "docker rm -f \$(docker ps -aq) || true"
                    }
                    }
            stage('build'){
            steps{
                     sh "docker build -t jenkinsimage ."
                    }
            }
            stage('run'){
            steps{
                     sh "docker run -d -p 80:5500 --name jenkins jenkinsimage"
                }
            }
        }
    }
