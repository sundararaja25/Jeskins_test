pipeline {
    agent { label "dev-master"}
    stages {
        stage('Checkout') {
            steps {
                    git(
                    url: "https://github.com/sundararaja25/Jeskins_test.git",
                    branch: "main",
                    changelog: true,
                    poll: true
               )
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
                echo ' Run test'
                //sh 'chmod +x run_tests.sh'
               // sh './run_tests.sh' // Assuming you have a script to run tests
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
