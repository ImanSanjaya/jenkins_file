pipeline {
    agent any

    stages {
        stage ('Process One') {

            steps {
                echo 'Hi, Saya Iman Sanjaya Dari FUSI'
            }
        }

        stage ('Process Two') {

            steps {
                input('Apakah kamu akan melanjutkan Proses?')
            }
        }


        stage ('Process Three') {
            
            when {
                not{
                    branch "main"
                }
            }
            steps {
                echo 'Anda Telah Memilih Untuk Melanjutkan Proses'
            }

        }

        stage ('Process Four') {

            paraller {

                stage ('Unit Test') {

                    steps {
                        input('Proses Unit Test Berjalan . . .')
                    }
                }

                stage ('Integration Test') {

                    agent {
                        docker {
                            reuseNode false
                            image 'ubuntu'
                        }
                    }
                    steps {
                        echo 'Running the integration test . . .'
                    }
                }

            }

        }
    }
}