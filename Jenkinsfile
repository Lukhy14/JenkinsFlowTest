pipeline {
  agent any
  stages {
    stage('TokenGet') {
      steps {
        bat(returnStatus: true, script: 'curl --silent --location --request POST \'https://testeqdepot.sugarondemand.com/rest/v11/oauth2/token?username=dm1&grant_type=password&client_id=sugar&password=Suavis*123&platform=apiCRM\' \\ --header \'Cookie: PHPSESSID=bf9ef178-18f7-4f2b-98da-95549d413b2d; download_token_apiCRM=1c067db1-2bb1-4104-aed2-376a55700c87; download_token_base=9812811e-6dbb-48e1-842f-a99237bc7be1\'', returnStdout: true, label: 'access_token', encoding: 'UTF-8')
        echo 'access_token'
      }
    }

  }
}