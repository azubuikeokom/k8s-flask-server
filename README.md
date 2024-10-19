I will leverage the use of AWS EKS to provision a kubernetes cluster. Kubernetes helps to provide optimized use of compute resource by ochestrating and managing container deployment on compute resources that form the worker nodes in a kubernetes cluster. In deplloying the cluster, I will define different node groups designated for certain kind of workloads, I will configure the installations of cluster addons such as CNI-addons, CSI-addons etc. I will make use of terraform to manage the entire infrastructure deployment, use helm where necessary, kustomize for targeting different environment and argocd for GitOps process.
Furthermore, I will deploy the use of build servers like Github actions for continuous integration process, where workflows will be setup in Github actions to manage the build of application images, integrating vulnerabilies check at the early stage of the deployment process. Built images will be automatically pushed to organization's private repository and tagged accordinly.
Rollout of new releases will be automated with argocd, which detects changes to kubernetes resource configuration files (deployments, jobs etc) in the organization's repo (Github) and syncs those changes with resources in the cluster.
Each environment cluster will be targeted by leveraging the use of applicationset to template different applications on different cluster environments.
The directory structure of the application deployment depicts the different cluster environment that argocd applicationset targets by the use of git generators.