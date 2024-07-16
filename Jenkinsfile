pipeline {
    agent any

    tools {nodejs "node"}

    stages {

        stage('Cypress Parallel Test Suite') {
            parallel {
                stage('Slave 1') {
                    agent {
                        label "Agent1_1"
                    }
                    steps {
                        git url: 'https://github.com/JAG3161/Cypress_2.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key e978b741-d418-44e3-b7a6-2716d147aad4  --parallel'
                        
                    
                    }
                }

                stage('Slave 2') {
                    agent {
                        label "Agent1_2"
                    }
                    steps {
                        git url: 'https://github.com/JAG3161/Cypress_2.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key e978b741-d418-44e3-b7a6-2716d147aad4  --parallel'
                    
                    }
                }

                stage('Slave 3') {
                    agent {
                        label "Agent1_3"
                    }
                    steps {
                        git url: 'https://github.com/JAG3161/Cypress_2.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key e978b741-d418-44e3-b7a6-2716d147aad4  --parallel'
                    
                    }
                }

                /*stage('Slave 4') {
                    agent {
                        label "Agent2_4"
                    }
                    steps {
                        git url: 'https://github.com/RodrigoUdemy/Paralelo_pipline.git'
                        bat 'npm install'
                        bat 'npm update'                       
                        bat 'npx cypress run cypress run --record --key 7f3ad08e-6c6e-442f-bcbd-cb3269ac5a9c  --parallel'
                    
                    }
                }*/

               

                
   
                  
            }

             
        }

    }
            
}