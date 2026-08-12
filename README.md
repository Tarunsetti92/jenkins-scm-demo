pipeline {
    agent any
    
    stages {
        
        stage('cloning'){
            steps {
                git clone 'https://github.com/Tarunsetti92/hipythonfastapi'
            }
        stage ('installing dependencies'){
            steps {
                sh '''
                python3 -m venv venv
                . venv/bin/activate
                pip install -r requirements.txt
                '''
                
            }
        }
        }
    }
}
