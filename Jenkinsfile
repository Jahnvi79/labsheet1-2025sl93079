pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Jahnvi79/labsheet1-2025sl93079.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build stage"'
                sh 'ls -l'
            }
        }

        stage('Test') {
            steps {
                sh '''
                python3 -c "
import calculator

# Test all functions
assert calculator.add(2,3) == 5
assert calculator.sub(5,3) == 2
assert calculator.mul(2,3) == 6
assert calculator.div(6,3) == 2

print('All tests passed successfully')
"
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy stage (dummy)"'
            }
        }
    }
}
