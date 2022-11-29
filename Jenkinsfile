pipeline {

    agent any

    environment {

        JFROG_CLI_BUILD_NAME = "${env.JOB_NAME}"

        JFROG_CLI_BUILD_NUMBER = "${env.BUILD_NUMBER}"

    }

    stages {

        stage ('Run JFrog CLI') {

            steps {

                sh 'jf -v'

                sh 'jf rt npm-install --build-name=npm-challenge-build --build-number=1.0.0'

                sh 'jf rt npm-install --build-name=npm-challenge-build --build-number=1.0.0'

                sh 'jf rt bce npm-challenge-build 1.0.0'
                
                sh 'jf rt bp npm-challenge-build 1.0.0'
                // sh 'jfrog rt mvn -f /path/to/pom.xml clean install' // build & deploy artifacts

                // sh 'jfrog rt bp' // publish build info

            }

        }

    }

}