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

     parameters {
        string(name: 'learning', defaultValue: 'Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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

        stage('testing params'){

            steps{
                    echo " ${params.learning} "
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