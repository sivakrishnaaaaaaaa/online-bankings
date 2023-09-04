pipeline{
    agent any
    stages{
        stage("maven build"){
            when {
                branch 'develop'
            }
            steps{
                sh "mvn cleanpackage"
            }
        }
        stage ("sonar analysis"){
            when {
                branch 'develop'
            }
            steps{
                echo "sonar analysis"
            }
        }
        stage ("dev deploy"){
            when {
                branch 'develop'
            }
            steps{
                echo "dev deploy..."
            }
        }
        stage("test deploy"){
            when {
                branch 'test'
            }
            steps {
                echo "test deploy..."
            }
        }
        stage ("prod deploy"){
            when {
                branch 'main'
            }
            steps {
                echo "prod deploy..."
            }
        }
    }
}