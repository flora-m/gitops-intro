# openshift-gitops
This directory contains the initial configuration to bootstrap gitops. Additional config is whithin ./apps/openshift-gitops. This configuration should be used to modify the config of gitops. 

Allow GitOps service account permissions to create namespaces and resources in OCP. In production, caution should be excercised when allocating these permissions and they should be used in conjuction with ArgoCD project roles. 
```
oc adm policy add-cluster-role-to-user cluster-admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller
```
