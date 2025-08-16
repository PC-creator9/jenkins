pipeline{
    agent {
        
        label 'agent-01'
 
}
    environment{

        agent_label = 'agent-01'
    }
// exploring options
    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds() 
    }

    stages{

        stage('first'){

            steps{
                    echo " jenkins pipleine script is working  "

            }
        }

         stage('testing env'){

            steps{
                    sh """
                        echo " the agent label is $agent_label "
                                    
                       """

            }
        }


    }
    // post-build-actions
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