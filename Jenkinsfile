pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Test Stage') {

            steps {
                withMaven(maven : 'Maven') {
                    bat 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Maven') {
                    bat 'mvn deploy'
                }
            }
        }
    }
}
