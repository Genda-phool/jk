pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning the repository...'
                git branch: 'main', url: 'https://github.com/Genda-phool/jk.git'
            }
        }

        stage('Run Script') {
            steps {
                echo 'Running the script...'
                sh './testscript.sh'
            }
        }

        stage('Print Success Message') {
            steps {
                echo 'Pipeline executed successfully!'
            }
        }
    }
}
