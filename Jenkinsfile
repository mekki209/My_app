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
}


}
