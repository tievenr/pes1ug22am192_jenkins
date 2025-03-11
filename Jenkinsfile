pipeline{
  agent any
  stages  {
    stage("Build")  {
      steps{
        sh "g++ main.cpp -o output"
        build "PES1UG22AM192-1"
      }
    }
    stage("Test")  {
      steps{
        sh "./output"
      }
    }
    stage("Deploy")  {
      steps{
        echo "Deploy"
      }
    }
  }
  post  {
    failure {
      error "Pipeline failed"
    }
  }
}