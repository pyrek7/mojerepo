pipeline {
    agent any
    environment {
       python3 = '"C:\\Program Files\\WindowsApps\\PythonSoftwareFoundation.Python.3.13_3.13.496.0_x64__qbz5n2kfra8p0\\python3.13.exe"'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Starting building python script'
                bat "${python3} code.py"
                echo 'Finishing building python script'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing from SCM..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying from SCM....'
            }
        }
    }
}
