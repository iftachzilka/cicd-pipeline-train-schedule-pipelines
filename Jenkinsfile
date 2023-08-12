pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                sh 'chmod +x /var/lib/jenkins/.gradle/wrapper/dists/gradle-8.2-milestone-1-bin/99cywuoc4xy2d7kadu1u5y1lx/gradle-8.2-milestone-1/bin/gradle'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
