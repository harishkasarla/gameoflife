node
{
  stage('checkout')
  {
  checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'PerBuildTag']], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/harishkasarla/gameoflife.git']]])
  }
}
