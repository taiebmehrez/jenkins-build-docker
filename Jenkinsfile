node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("xavki/nginx")
    }

    stage('Run image') {
        docker.image('xavki/nginx').withRun('-p 82:82') { c ->

        sh 'docker ps'

        sh 'curl localhost'

    }

    }
    
}
