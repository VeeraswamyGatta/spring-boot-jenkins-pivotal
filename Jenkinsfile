pipeline {
    agent any

    stages {
        stage ('Compile Stage') {
            steps {
                withMaven(maven : 'Maven3.6') {
                    sh 'mvn clean install'
                }
            }
        }

        stage ('Testing Stage') {
            steps {
                withMaven(maven : 'Maven3.6') {
                    sh 'mvn test'
                }
            }
        }

        stage ('Deployment Stage') {
            steps {
		            withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'PCF_LOGIN',
                            usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD']]) {

                    sh 'C:/Veeraswamy/Softwares/cf-cli_6.46.0_winx64/cf login -a http://api.run.pivotal.io -u $USERNAME -p $PASSWORD'
			        sh 'C:/Veeraswamy/Softwares/cf-cli_6.46.0_winx64/cf push'
                }
            }
        }
    }
}