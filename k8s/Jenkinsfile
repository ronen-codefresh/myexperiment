node {
   stage("echo 1") {
      echo 'Starting deployment'
   }
   stage("deploy") {
   
      kubernetesDeploy(kubeconfigId: 'kubeconfig-staging',               // REQUIRED

                  configs: 'k8s/*.yaml', // REQUIRED
                  enableConfigSubstitution: false
      )
   }
 
   stage("echo 2") {
   
      echo 'deployment ended'
   }
}