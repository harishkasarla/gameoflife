node
{
  stage('checkout')
  {
  checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'PerBuildTag']], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/harishkasarla/gameoflife.git']]])
  }
  stage('Mvn Package')
  {
    def mvnHome = tool name: 'maven-3', type: 'maven'
    def mvnCMD = "${mvnHome}"
    sh 'mvn clean package'
  }
  stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
  }
