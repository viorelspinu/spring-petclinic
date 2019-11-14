pipeline {
    agent any

    environment {
        MAVEN_INSTALLATION = 'maven-installation'
        MAVEN_SETTINGS_CONFIG = '3b8a7cc8-9573-410d-92ea-9e6aa9ce7644'
    }

    stages {
        stage('Build') {
            steps {
                withMaven(maven: MAVEN_INSTALLATION, mavenSettingsConfig: MAVEN_SETTINGS_CONFIG) {
                    sh 'mvn -DskipTests clean package'
                }
            }
        }

        stage('Test') {
            steps {
                withMaven(maven: MAVEN_INSTALLATION, mavenSettingsConfig: MAVEN_SETTINGS_CONFIG) {
                    sh 'mvn test'
                }
            }
        }
    }
}