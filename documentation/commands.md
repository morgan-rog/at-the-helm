**Configuring kubectl after deploying GKE**
```
gcloud container clusters get-credentials $(terraform output -raw kubernetes_cluster_name) --region us-central1-f
```

**Add yourself as cluster administrator in the cluster's RBAC so that you can give Jenkins permissions in the cluster**
```
kubectl create clusterrolebinding cluster-admin-binding \
  --clusterrole=cluster-admin --user=$(gcloud config get-value account) -n jenkins
```
**Add the Jenkins Helm chart repository and install Jenkins**
```
helm repo add jenkinsci https://charts.jenkins.io

helm repo update

kubectl create namespace jenkins

helm install cd-jenkins -f jenkins-configuration/values.yaml jenkinsci/jenkins -n jenkins --wait
```
**Get Jenkins password**
```
kubectl exec --namespace jenkins -it svc/cd-jenkins -c jenkins -- /bin/cat /run/secrets/additional/chart-admin-password && echo
```