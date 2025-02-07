pipeline{
    agent any
    tools{
        maven 'mymaven'
    }
    stages{
        stage('clone Repo'){
            steps{
                git 'https://github.com/vishukanojiya/DevOpsJava.git'
            }
        }
        stage('CompileCode'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('ReviewCode'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('TestCode'){
            steps{
                sh 'mvn test'
            }
        }
        stage('BuildCode'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
