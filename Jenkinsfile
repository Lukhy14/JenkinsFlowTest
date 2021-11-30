pipeline {
  agent any
  stages {
    stage('TokenGet') {
      steps {
        bat(returnStatus: true, script: 'curl --location --request POST \'https://testeqdepot.sugarondemand.com/rest/v11/oauth2/token?username=dm1&grant_type=password&client_id=sugar&password=Suavis*123&platform=apiCRM\' \\ --header \'Cookie: PHPSESSID=ce261859-8b5a-401c-bb18-61510c50b40d; download_token_apiCRM=0b196fdd-aeef-4fb1-abac-9cb1b17727ad; download_token_base=9812811e-6dbb-48e1-842f-a99237bc7be1\'', returnStdout: true, label: 'access_token', encoding: 'UTF-8')
      }
    }

  }
}