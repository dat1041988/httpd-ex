node('') {
          stage 'build'
          openshiftBuild(namespace: 'datpb-http', buildConfig: 'httpd-ex', showBuildLogs: 'true')
          stage('Deploy approval'){
            input "Deploy to prod?"
            }
          stage 'deploy'
          openshiftDeploy(namespace: 'datpb-http', deploymentConfig: 'httpd-ex')
        }
