# gke-test-playground-argocd

This is a playground for me to test out GKE and play around with kuberentes.

# Docs

- Create Cluster
- helm repo add external-secrets https://charts.external-secrets.io
- helm template crossplane crossplane-stable/crossplane -n crossplane-system --include-crds --namespace crossplane -f values.yaml > install.yaml
- helm template external-secret/external-secrets --include-crds --namespace kube-addons > install.yaml
- helm repo update
- Do Crossplane Things
- kubectl apply -k namespaces/
- k apply -k crossplane/
- Install ArgoCD

# Done
- Deployment for Nginx
- Service for Nginx
- Kustomize for Nginx
- Ingress Controller Support
- Expand Ingress Controller
- HPA support
- Created Service Account in GCP
- Created Crossplane with ServiceAccount Annotations
- 
# Expansion
- ArgoCD Support
- HTTPS support
- Frontend // React with Secrets
- Backend // NodeJS with Secrets
- Small SQL server // Cloud SQL?
- ExternalSecret
- Creation of multiple namespaces
- Crossplane Support // creating the Cloud SQL server
- ArgoCD with App of App pattern
- In the certain number of resources
- Create a Helm version of the application




# Next Step 
<!---# - Use the Cluster SA Account to in the ClusterSecretStore NOT NEEDED
# - Create Service Role for Secret Management NOT NEEDED
# - Pull Secret into the actual crossplane namespace NOT NEEDED -->
- Read up on GKE Workload Identity
- Crossplane to create a SQL Server
<!--- # - External Secrets -->
- Frontend // React with Secrets
	- Create React FE - Application is a Colorbackground App? 
	- External Secrets in GKE 



gcloud iam service-accounts add-iam-policy-binding crossplane-sa-test@test-projects-376916.iam.gserviceaccount.com --role roles/iam.workloadIdentityUser --member "serviceAccount:test-projects-376916.svc.id.goog[crossplane/crossplane]"

kubectl run -i --tty test3 --image gcr.io/cloud-builders/gsutil ls gs://workload-identity-test --serviceaccount=crossplane -n crossplane