# gke-test-playground-argocd

This is a playground for me to test out GKE and play around with kuberentes.

# Docs

- Create Cluster
- helm repo add external-secrets https://charts.external-secrets.io
- helm template crossplane crossplane-stable/crossplane -n crossplane-system
- helm repo update
- Do Crossplane Things
- Install ArgoCD

# Done
- Deployment for Nginx
- Service for Nginx
- Kustomize for Nginx
- Ingress Controller Support
- Expand Ingress Controller
- HPA support

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
- Secret Management First
- Create Service Role for Secret Management
- Pull Secret into the actual crossplane namespace
- Crossplane to create a SQL Server
- External Secrets
- Frontend // React with Secrets
	- Create React FE - Application is a Colorbackground App? 
	- External Secrets in GKE 

