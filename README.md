# Plugins Jenkins
kubernetes

# Informations du cluster
kubectl cluster-info

# Url du Dashboard kubernetes
Dashboard: https://localhost:32000/

https://www.replex.io/blog/how-to-install-access-and-add-heapster-metrics-to-the-kubernetes-dashboard
## Creation d'un service account pour le dashboard
kubectl create serviceaccount dashboard-admin-sa

kubectl create clusterrolebinding dashboard-admin-sa --clusterrole=cluster-admin --serviceaccount=default:dashboard-admin-sa

kubectl get secrets

kubectl describe secret dashboard-admin-sa-token-kw7vn

# Slave jnlp Jenkins
Slave : jenkinsci/jnlp-slave

# Kubernetes ServiceAccount for Jenkins 
kubectl create serviceaccount jenkins -n cicd

Retrieve Service Account Token in jenkins-token-* secret

echo "secrer_retrived" | base64 --decode 

Save the secret as Jenkins Secret Text credentials

Use the decode CA to configure the cloud part

