node {
    def root = "/usr/local/go/bin/go"

    stage 'Checkout'
    // git url: 'https://github.com/giovanniRisrian/sample-go-jenkins.git'
    git branch: "main", url: 'https://github.com/giovanniRisrian/sample-go-jenkins.git' 
        
    stage 'preTest'
    sh "${root} version"

    stage 'Test'
    sh "${root} test ./... -cover"

    stage 'Build'
    sh "${root} build ./..."

}