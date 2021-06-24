pipeline {
    agent any 
        stages {
                stage('pull code') {
                    steps {
                        echo 'This is first step for git repo pull'
                    }                    
                }
        
                stage ('Build') {
                    steps {                        
                        echo 'This stage will do the code build'
                    }
                }
                stage ('Code Quality') {
                    steps {
                         echo 'This stage will do the code quality'
                    }
                }
                stage ('Artifacts') {
                    steps {
                         echo 'push the artifact to AMS'
                    }
                   
                }
                stage ('Test') {
                              steps {
                                        echo 'Running Integration Test'
                                    }

                                }
                }
        
}