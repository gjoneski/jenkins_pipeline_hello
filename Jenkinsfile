#!groovy

node {
  def testVar = "test"
  def hash = sh(returnStdout: true, script: "git log -n 1 --pretty=format:'%h'").trim()
  stage('Stage 1') {
    echo "Hello ${testVar}"
    echo "Hello ${hash}"
    echo "Hello World 1"
    checkout scm
    sh "git rev-parse HEAD > commit"
    def commit = readFile("commit").trim()
    echo "git commit: ${commit}"
    sh " sed -i -e 's/__COMMIT_HASH_PLACEHOLDER__/${commit}/' hash_placeholder.txt "
    def fileContent = readFile("hash_placeholder.txt")
    echo "file content: ${fileContent}"
  }

   stage "Stage 2"
   		echo "Hello World 2"
}
