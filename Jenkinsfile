pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                withAWS(region:'eu-central-1',credentials:'yourIDfromStep2') {

                    // def identity=awsIdentity();//Log AWS credentials

                    // Upload files from working directory 'dist' in your project workspace
                    s3Upload(bucket:"subrockmann-ud-jenkins", file:'index.html', path:'index.html')
                }
            }
        }
    }
}