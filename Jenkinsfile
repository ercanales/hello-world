node('ssh') {
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'TestGit', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/ercanales/hello-world.git']]])
}
