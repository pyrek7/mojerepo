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
        stage('ParallelScript') {
            steps {
                parallel (
                    "TaskOne" : {
                        echo 'task one stuff part 1'
                        echo 'task one stuff part 2'
                        echo 'task one stuff part 3'
                    },
                    "TaskTwo" : {
                        echo 'task two stuff part 1'
                        echo 'task two stuff part 2'
                    },
                    "TaskThree" : {
                        echo 'task three stuff part 1'
                        echo 'task three stuff part 2'
                    }
                    )
            }
        }
    }
}
