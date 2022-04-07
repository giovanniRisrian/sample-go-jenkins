pipeline{
    agent any 
    environment {
        root = "/usr/local/go/bin/go"
        branch = "main"
        scmUrl = 'https://github.com/giovanniRisrian/sample-go-jenkins.git'
    }

    stages {
        stage("Go Version") {
            steps {
                sh "${root} version"
            }
        }
        stage("Go Clone") {
            steps {
                git branch: "main", url: 'https://github.com/giovanniRisrian/sample-go-jenkins.git' 
    
            }
        }
        stage("Go Test") {
            steps {
                sh "${root} test ./... -cover"
            }
        }
        stage("Go Build") {
            steps {
                sh "${root} build ./..."
            }
        }
        
    }
}

// node {
//     def root = "/usr/local/go/bin/go"

//     stage 'Checkout'
//     git branch: "main", url: 'https://github.com/giovanniRisrian/sample-go-jenkins.git' 
        
//     stage 'preTest'
//     sh "${root} version"

//     stage 'Test'
//     sh "${root} test ./... -cover"

//     stage 'Build'
//     sh "${root} build ./..."

// }