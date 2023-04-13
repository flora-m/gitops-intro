# openshift-gitops
This repository demonstrates the use of an ApplicationSet to deploy an  App of Apps GitOps pattern. Applications are container whithin ./apps/* and the configuration to bootstrap the ApplicationSet is contained in ./init-gitops.yaml.

Allow GitOps service account permissions to create namespaces and resources in OCP. In production, caution should be excercised when allocating these permissions and they should be used in conjuction with ArgoCD project roles. 
```
oc adm policy add-cluster-role-to-user cluster-admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller
```
