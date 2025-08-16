pipeline{
    agent {
        
        label 'temp'
 
}
    stages{

        stage('first'){

            steps{
                    echo " jenkins pipleine script is working  "

            }
        }


    }
    post { 
        failure { 
            echo 'pipleine is failed'
        }
        success { 
            echo 'pipleine is succesful.. yayy!!!!'
        }
        always { 
            echo 'Im here always - post build '
        }
    }
}    