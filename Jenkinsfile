pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                def withMaven(maven) {
                    sh 'mvn clean compile'
                }
				withMaven(localMaven)
            }
        }

        stage ('Testing Stage') {

            steps {
                def withMaven(maven) {
                    sh 'mvn test'
                }
				withMaven(localMaven)
            }
        }


        stage ('Deployment Stage') {
            steps {
                def withMaven(maven) {
                    sh 'mvn deploy'
                }
				withMaven(localMaven)
            }
        }
    }
}
