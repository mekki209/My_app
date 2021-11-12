pipeline {
    agent any
      stages{
         stage('Pull'){
            steps {
              script{
                  checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                       userRemoteConfigs: [[
                          credentialsId:'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',
                          url: 'https://github.com/mekki209/My_app.git']]])

                     }

            }
        }

stage('build')
{
                  steps {
                         script{
                         sh "ansible-playbook my-app/Ansible/build.yml -i my-app/Ansible/inventory/host.yml "
                                }
                        }
  }


}
}
