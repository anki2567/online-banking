pipeline{
    agent any
    stages{
        stage("Maven Build"){
            when{
                branch 'develop'
            }
            steps{
                sh "mvn clean package"
        }
    }
    stage("Sonar Analysis"){
             when{
                branch 'develop'
            }
            steps{
                echo "Sonar Analysis"
        }
    }
    stage("Dev Deploy"){
        when{
            branch 'develop'
        }
            steps{
                echo "Dev Deploy..."
        }
    }
    stage("Test Deploy"){
        when{
            branch 'test'
        }
            steps{
                echo "test Deploy..."
        }
    }
    stage("Prod Deploy"){
        when{
            branch 'main'
        }
            steps{
                echo "prod Deploy..."
        }
    }
}



}