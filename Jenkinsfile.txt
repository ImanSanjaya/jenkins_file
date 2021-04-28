pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                echo 'On Process Compile Stage'
            }
        }

        stage ('Testing Stage') {

            steps {
                echo 'On Process Testing Stage'
            }
        }


        stage ('Deployment Stage') {
            
            steps {
                echo 'On Process Deployment Stage'
            }

        }
    }
}