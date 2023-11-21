pipeline{

    agent any
    tools{
        maven 'maven'
        }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -B compile'
                }
            }
        stage('Test'){
            steps{
                sh 'mvn -B clean install'
                }
            }
        stage('Archive'){
            steps{
                archiveArtifacts 'target/*.jar'
                }
            }
        }
    }