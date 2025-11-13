This repository is to trigger ArgoCD when any changes are commited to this repository.

Argo is running on my local but pointing to this Git repo from the Application.yaml in line:
repoURL: https://github.com/Javi-Jmnz/argocd

To Install ArgoCD in local machine run:

kubectl create namespace argocd

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

To apply the changes from your application.yaml run:
kubectl apply -f application.yaml

In local go to: https://localhost:8081/applications/argocd/javi-nginx-app?conditions=false&view=tree&resource=
