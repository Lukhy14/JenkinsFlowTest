pipeline {
  agent any
  stages {
    stage('TokenGet') {
      steps {
        bat(returnStatus: true, script: 'curl --silent --location --request POST \'https://testeqdepot.sugarondemand.com/rest/v11/oauth2/token?username=dm1&grant_type=password&client_id=sugar&password=Suavis*123&platform=apiCRM\' \\ --header \'Cookie: PHPSESSID=bf9ef178-18f7-4f2b-98da-95549d413b2d; download_token_apiCRM=1c067db1-2bb1-4104-aed2-376a55700c87; download_token_base=9812811e-6dbb-48e1-842f-a99237bc7be1\'', returnStdout: true, label: 'TokenOutput', encoding: 'UTF-8')
        echo '$ReturnStatus'
        powershell(script: '$headers = New-Object "System.Collections.Generic.Dictionary[[String],[String]]" $headers.Add("Cookie", "PHPSESSID=b158d610-fcae-4501-976a-e767693c1c95; download_token_apiCRM=bc5f3734-883a-43cd-b996-d146cd246d6b; download_token_base=9812811e-6dbb-48e1-842f-a99237bc7be1")  $response = Invoke-RestMethod \'https://testeqdepot.sugarondemand.com/rest/v11/oauth2/token?username=dm1&grant_type=password&client_id=sugar&password=Suavis*123&platform=apiCRM\' -Method \'POST\' -Headers $headers $response | ConvertTo-Json', returnStatus: true, returnStdout: true)
      }
    }

  }
}