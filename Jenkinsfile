stage('build') {
parallel build1: {node{
    deleteDir()
   checkout scm
   sh label: '', script: 'echo hello world > hello.txt'
   archiveArtifacts '*.txt'
   sleep 10
    deleteDir()
}},
build2: {node{
    deleteDir()
    checkout scm
   sh label: '', script: 'echo goodbye world > goodbye.txt'
   archiveArtifacts '*.txt,*.md'
   sleep 10
    deleteDir()
}}
}
