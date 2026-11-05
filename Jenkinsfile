pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building HospiSync Backend'
                bat 'mvnw.cmd -B clean package -DskipTests'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
}
