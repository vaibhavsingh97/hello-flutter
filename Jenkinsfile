pipeline {
    agent any

    stages {
        stage('Create Build') {
            steps {
                // Set up Flutter SDK
                sh 'flutter config --no-analytics'
                sh 'flutter doctor'
                sh 'flutter clean'
                // Get dependencies
                sh 'flutter pub get'
                sh 'flutter test'
                // Build the app
               // sh 'flutter build apk'  // for Android
                sh '''
                    #!/bin/sh
                    flutter build apk --debug
                '''
                // or
                // sh 'flutter build ios'  // for iOS

            }
        }
    }
}
