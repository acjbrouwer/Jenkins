# Installing Jenkins on K8s

Documentation:
-  https://www.jenkins.io/doc/book/installing/kubernetes/
   * https://www.jenkins.io/doc/book/installing/kubernetes/#install-jenkins-with-helm-v3
     + https://github.com/jenkinsci/helm-charts

## Bitnami Helm chart

https://github.com/jenkinsci/helm-charts
`kubectl apply -f role-rolebinding.yaml`

## Walk throughs

**DEV Community:** https://dev.to/bravinsimiyu/how-to-setup-jenkins-on-kubernetes-cluster-with-helm-5an 

Basically follows the official documentation, but adds a few
explanations. Does not go into customization.

**Octopus Deploy:** https://octopus.com/blog/jenkins-helm-install-guide

Explains how to:
- Deploy Jenkins to Kubernetes with Helm.
- Expose Jenkins on a public IP address.
- Install additional plugins as part of the installation process.
- Configure Jenkins through JCasC.
- Backup the Jenkins home directory.
- Create Kubernetes agents that are created and destroyed as needed.

**Redgate’s Simple Talk:** https://www.red-gate.com/simple-talk/devops/ci-cd/how-to-set-up-jenkins-ci-cd-on-kubernetes-cluster-using-helm/ This article provides a comprehensive guide on setting up Jenkins CI/CD on a Kubernetes cluster using Helm. It covers the prerequisites, installation steps, and how to get your admin password for unlocking Jenkins.
