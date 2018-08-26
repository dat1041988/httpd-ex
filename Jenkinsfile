node('') {
          stage 'build'
          openshiftBuild(namespace: 'datpb-http-canary', buildConfig: 'httpd-ex', showBuildLogs: 'true')
          stage('Deploy approval'){
            input "Deploy to prod?"
            }
          stage 'deploy'
          openshiftDeploy(namespace: 'datpb-http-canary', deploymentConfig: 'httpd-ex')
        }
