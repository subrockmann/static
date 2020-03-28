pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                withAWS(region:'eu-central-1',credentials:'Jenkins') {

                    // def identity=awsIdentity();//Log AWS credentials

                    // Upload files in your project workspace
                    s3Upload(bucket:"subrockmann-ud-jenkins", file:'index.html', path:'index.html');
                }
            }
        }
    }
}