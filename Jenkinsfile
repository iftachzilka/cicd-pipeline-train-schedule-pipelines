pipeline {
  agent any
  stages{
    stage ('Build'){
      steps{
        echo "Running build automation"
        sh 'chmod +x /var/lib/jenkins/.gradle/wrapper/dists/gradle-4.6-bin/4jp4stjndanmxuerzfseyb6wo/gradle-4.6/bin/gradle'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
