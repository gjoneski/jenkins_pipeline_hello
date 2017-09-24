#!groovy

node {
  stage 'Stage 1' {
    echo 'Hello World 1'
    sh 'git rev-parse HEAD > commit'
    def commit = readFile('commit').trim()
    echo "git commit: ${commit}"
  }

   stage 'Stage 2'
   		echo 'Hello World 2'
}
