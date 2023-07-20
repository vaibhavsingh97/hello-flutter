pipeline {
    agent any

    stages {
        stage('Create Build') {
            steps {
                // Set up Flutter SDK
                sh 'flutter config --no-analytics'
                sh 'flutter doctor'
                sh 'flutter test'
                // Get dependencies
                sh 'flutter pub get'

                // Build the app
                sh 'flutter build apk'  // for Android
                // or
                // sh 'flutter build ios'  // for iOS

                // Optionally, run tests
                // sh 'flutter test'
            }
        }
    }
}
