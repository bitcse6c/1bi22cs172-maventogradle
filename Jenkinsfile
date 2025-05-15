pipeline {
    agent any  

    tools {
        maven 'Maven'
        gradle 'Gradle'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/bitcse6c/1bi22cs172-maventogradle.git'
        }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'  // Run Maven build
        }
        }


        
        
       
        stage('Run Application') {
            steps {
                sh 'mvn exec:java -Dexec.mainClass="com.example.App" '
        }
        }

        
    }

    post {
        success {
            echo 'Build successful'
        }
        failure {
            echo 'Build failed'
}
}
}
