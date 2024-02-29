pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your Git repository
                git 'https://manoharans@git.i2r.a-star.edu.sg/manoharans/Test_Jenkins.git'
            }
        }
        stage('Build') {
            steps {
                // Create a build directory and change to it
                dir('build') {
                    // Generate Makefiles using CMake
                    sh 'cmake ..'
                    
                    // Build the project
                    sh 'make'
                }
            }
        }
        stage('Test') {
            steps {
                // Run your tests here if you have any
                sh './run_tests.sh' // Assuming you have a script to run tests
            }
        }
        stage('Deploy') {
            steps {
                // Deployment steps if needed
                echo 'Deployment steps go here'
            }
        }
    }
}
