pipeline {
  agent any
  stages{
    stage ('Build'){
      steps{
        echo "Running build automation"
        sh './gradlew build --no-daemon'
        sh 'chmod +x /var/lib/jenkins/.gradle/wrapper/dists/gradle-4.6-bin/4jp4stjndanmxuerzfseyb6wo/gradle-4.6/bin/gradle'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
