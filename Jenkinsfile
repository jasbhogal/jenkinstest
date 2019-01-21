stage('build') {
parallel build1: {node{
    deleteDir()
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/jasbhogal/jenkinstest.git']]])
   sh label: '', script: 'echo hello world > hello.txt'
   archiveArtifacts '*.txt'
   sleep 10
    deleteDir()
}},
build2: {node{
    deleteDir()
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/jasbhogal/jenkinstest.git']]])
   sh label: '', script: 'echo goodbye world > goodbye.txt'
   archiveArtifacts '*.txt,*.md'
   sleep 10
    deleteDir()
}}
}
