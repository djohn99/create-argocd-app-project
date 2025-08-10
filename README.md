# create-argocd-app-project
This is to create Project or application on argocd

# Consumer Actions Service

This service can be deployed to Kubernetes via ArgoCD using our **Reusable Deployment Template**  
The template automatically:
- Creates/updates an ArgoCD **Project** (`<service>-<environment>`)
- Creates/updates an ArgoCD **Application** pointing to this service's manifests
- Enables ArgoCD auto-sync, prune, and self-heal

---

## 🚀 Deploy via GitHub Actions

1. Go to **Actions** tab in this repository.
2. Select **"Deploy Service via ArgoCD Template"** workflow.
3. Click **"Run workflow"** and fill in:
   - **service_name** → This service's name, e.g. `consumer-actions`
   - **environment** → Target environment, e.g. `dev`, `sit`, `stg`, `uat`
   - **repo_url** → Git repo with manifests or Helm values, e.g.  
     `https://github.com/your-org/valuesFile.git`
   - **target_revision** → Git branch/tag/commit, e.g. `master`

4. Click **Run** and watch the deployment in:
   - GitHub Actions logs
   - ArgoCD UI → Project & Application will appear automatically

---

## 📄 Documentation

Full details on:
- Template inputs
- Generated YAML structure
- Conventions (naming, namespaces, repo paths)
- Requirements
