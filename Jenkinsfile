node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t docker_test:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'crono2' -p 'devops@2019' "
sh "docker tag docker_test:latest crono2/docker_test:express"
sh "docker push crono2/docker_test:express"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}