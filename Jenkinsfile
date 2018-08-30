node {
    def legion = load legion()

    legion.pod(ram: '1Gi') {
        stage('clone repo'){
            checkout scm
        }
        
        stage('run notebook'){
            legion.runNotebook('Income.ipynb')
        }

        stage('build'){
            legion.build()
        }

        stage('deploy'){
            legion.deploy()
        }
    }
}