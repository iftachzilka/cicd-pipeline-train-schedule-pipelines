pipeline {
  agent any
  stages{
    stage ('Build'){
      steps{
        echo "Running build automation"
        sh './gradlew build --no-daemon'
        sh 'chmod +x /var/lib/jenkins/.gradle/wrapper/dists/gradle-8.2-bin/bbg7u40eoinfdyxsxr3z4i7ta/gradle-8.2/bin/gradle'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
