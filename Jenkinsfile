pipeline{
 agent any
 environment{
  NEW_VERSION = '1.3.0'
  SERVER_CREDENTIALS = credentials('server-credentials')
 }
 parameters{
  booleanParam(name:'executetests' , defaultValue:false , description:'test execution wrt value')
 }
 stages{
  stage("build"){
    steps{
      echo "building the application"
      echo "building version ${NEW_VERSION}"
    }
  }
  stage("test"){
   when{
    expression{
      params.executetests == true
    }
   }
    steps{
      echo "testing the application"
      echo "testing version ${NEW_VERSION}"
    }
  }
  stage("deploy"){
    steps{
      echo "deploying the application"
      echo "deploying version ${NEW_VERSION}"
     echo "deploying with ${SERVER_CREDENTIALS}"
    }
  }
 }
}
