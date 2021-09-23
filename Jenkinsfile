pipeline {
    agent{label 'master'}
    tools{maven 'MAVEN_HOME'}
    stages {
        stage ('Checkout'){
            steps {
               git branch: 'main', url: 'https://github.com/divyeshpatel777/SpringPetClinic.git'
            }
        }
        stage ('Build') {
            steps {
                bat 'mvn compile'
            }
        }
        stage ('test') {
            steps {
               bat 'mvn test'
            }
        }
        stage ('Package') {
            steps {
               bat 'mvn package'
            }
        }
        stage ('Deploy') {
            steps {
               bat 'java -jar C:/Users/divypate/.jenkins/workspace/PetClinicDeclaritivePipeline/target/spring-petclinic-2.1.0.BUILD-SNAPSHOT.jar'
            }
        }
    }
}
