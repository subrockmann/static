pipeline {
    agent any
    stages {
        stage('Lint HTML'){
            steps{
                sh "tidy -q -e *.html"
            }
        }
        stage('Upload to AWS') {
            steps {
                withAWS(region:'eu-central-1',credentials:'Jenkins') {

                    s3Upload(bucket:"subrockmann-ud-jenkins", file:'index.html', path:'index.html');
                }
            }
        }
    }
}