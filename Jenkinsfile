pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'M2_HOME') {
                    sh 'clean package'
                }
            }
        }

        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'M2_HOME') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
