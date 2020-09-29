pipeline{
    agent any
    stages{
        stage("Hello World!!"){
            steps{
                echo "========executing A========"
                sh 'ls -la'
            }
        }
        stage("dir"){
            steps{
                sh 'pwd'
                echo "Major number is : ${params.Major}"
                echo "Minor Number is : ${params.Minor}"
                echo "Final Semantic versioning is : " +Major + "." +Minor
            }
        }
        stage("DockerBuild"){
            steps{
                sh "/usr/local/bin/docker build --tag trial:${Major}.${Minor} ."
            }
        }
    }   
}
