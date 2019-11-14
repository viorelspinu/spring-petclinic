stage('Test') {
    steps {
        withMaven(maven: 'maven-installation', mavenSettingsConfig: 'maven-settings.xml') {
            sh 'mvn test'
        }
    }
}