node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t devopsexam:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'mkemei' -p 'carola135/V' "
sh "docker tag devopsexam:latest mkemei/devopsexam:latest"
sh "docker push mkemei/devopsexam:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}

