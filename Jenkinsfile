node {
   stage("echo 1") {
      echo 'Starting deployment'
   }
   stage("deploy") {
   

//      kubernetesDeploy(kubeconfigId: 'kubeconfig-staging',               // REQUIRED
  //                configs: '**/*.yaml', // REQUIRED
    //              enableConfigSubstitution: false
      //)

      kubernetesDeploy configs: 'k8s/*.yaml', kubeConfig: [path: ''], kubeconfigId: 'kubeconfig-staging', secretName: '', ssh: [sshCredentialsId: '*', sshServer: ''], textCredentials: [certificateAuthorityData: '', clientCertificateData: '', clientKeyData: '', serverUrl: 'https://']
   }
 
   stage("echo 2") {
   
      echo 'deployment ended'
   }
}