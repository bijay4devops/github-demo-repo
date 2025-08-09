pipeline {
     agent any
         stages{
            stage('HELLO'){
              steps{
                 echo "hello world"
              }
            }
            stage(SCM){
                stpes{
                  echo "2nd stage pipeline code from github"
                }
            }
         }
}
