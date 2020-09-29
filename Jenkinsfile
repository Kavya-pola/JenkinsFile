pipeline{
 agent any
 stages{
  stage("clean"){
   steps{
    script{
     mvn clean test
    }
   }
  }
  stage("build"){
    steps{
      echo "building the application"
    }
  }
  stage("test"){
    steps{
      echo "testing the application"
  }
  }
  stage("deploy"){
    steps{
      echo "deploying the application"
   }
  }
 }
}
