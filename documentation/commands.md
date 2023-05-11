**Configuring kubectl after deploying GKE**
- gcloud container clusters get-credentials $(terraform output -raw kubernetes_cluster_name) --region us-central1-f