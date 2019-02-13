pipeline {
    agent any

    stages {
        stage('Deployment') {
            steps {
              sh '''
              kubectl apply -f deployments/envoy-initializer.yaml
              kubectl apply -f configmaps/envoy-initializer.yaml
                kubectl apply -f deployments/helloworld.yaml
                '''
            }
        }

    }
}
