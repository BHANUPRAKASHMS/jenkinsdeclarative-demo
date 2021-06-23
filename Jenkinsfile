pipeline {
    agent any 
        stages {
                stage('pull code') {
                    echo 'This is first step for git repo pull'
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
                    echo 'push the artifact to AMS'
                }
                stage ('Test') {
                            parallel {
                                stage ('Unit Test'){
                                        steps {
                                            echo ' Running unit tests.....'
                                           }
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
                                        echo 'Running Integration Test'
                                    }

                                }
                }
        }
}