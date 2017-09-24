#!groovy

node {
  stage('Stage 1') {
    echo "Hello World 1"
    checkout scm
    sh "git rev-parse HEAD > commit"
    def commit = readFile("commit").trim()
    echo "git commit: ${commit}"
    sh "sed -i '' 's/__COMMIT_HASH_PLACEHOLDER__/${commit}/' hash_placeholder.txt"
    def fileContent = readFile("hash_placeholder.txt")
    echo "file content: ${fileContent}"
  }

   stage "Stage 2"
   		echo "Hello World 2"
}
