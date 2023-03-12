pipeline {
    agent { label 'gol'}
    trigger {
        pollscm {'* * * * *'}
    }
    stages {
        stage ('git') {
            step {
             git branch: 'master',
             url: 'https://github.com/rudraramya/StudentCoursesRestAPI.git'
            }
        }
        stage ('docker') {
             step {
               sh 'docker image build -t apirest:1.0 .'
               sh 'docker tag apirest:1.0 rudras143/apirest:1.2'
                }
            }
        }
            }
