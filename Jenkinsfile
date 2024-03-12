pipeline{
  agent any
  stages{
    stage(Git Checkout){
      Steps{
              git branch: 'main', url: 'https://github.com/Devendra-Reddy-420/chatbt'
          }
    }
    stage(Maven Build){
      Steps{
              sh 'mvn clean package'
          }
    }
    stage(Dev-Deploy){
      when {
                branch 'develop'
            }
      Steps{
              echo "dev Deploy"
          }
      stage(Test-Deploy){
        when {
                branch 'test'
            }
      Steps{
              echo "Test Deploy"
          }
        stage(Prod-Deploy){
          when {
                branch 'main'
            }
      Steps{
             echo "Prod Deploy"
          }
    }
  }
}
