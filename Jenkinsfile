node('') {
          stage 'build'
          openshiftBuild(namespace: 'datpb-http', buildConfig: 'httpd-ex', showBuildLogs: 'true')
          stage 'deploy'
          openshiftDeploy(namespace: 'datpb-http', deploymentConfig: 'httpd-ex')
        }