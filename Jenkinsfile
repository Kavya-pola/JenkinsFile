pipeline{
 agent any
 stages{
  stage("build"){
    steps{
      echo "building the application dev"
    }
  }
  stage("test"){
   when{
    expression{
     BRANCH_NAME == 'dev'
    }
   }
    steps{
      echo "testing the application dev"
    }
  }
  stage("deploy"){
    steps{
      echo "deploying the application dev"
    }
  }
 }
}
