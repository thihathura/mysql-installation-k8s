Create Secret File
  kubectl apply -f sql-secret.yaml

Create Deployment File
  kubectl apply -f sql-deployment.yaml
  
Expose Service
  kubectl apply -f sql-service.yaml

Create Debug Container for Test
  1st Create Pod
  kubectl run pod debug --image=thihathura/test-container 
  2nd Login to Container
  kubectl exec -it debug -- bash
  3th Login to Mysql DB 
  mysql -h <mysql pod ip> -u root -p 
  4th Type the password that put into the secret file.
