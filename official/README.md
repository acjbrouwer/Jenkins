Steps to set up Jenkins YAML for deploying on Docker Desktop starting
with the verbatim example at
https://www.jenkins.io/doc/book/installing/kubernetes/#install-jenkins-with-helm-v3

Copy the YAML from the GitHub raw user content entries under
https://www.jenkins.io/doc/book/installing/kubernetes/#install-jenkins-with-helm-v3
to
`jenkins-sa.yaml`
`jenkins-volume.yaml`
`jenkins-values.yaml`

To prevent Helm installation errors, edit `jenkins-sa.yaml` as follows:
```
 metadata:
   name: jenkins
   namespace: jenkins
+  labels:
+    app.kubernetes.io/managed-by: Helm
+  annotations:
+    meta.helm.sh/release-name: jenkins
+    meta.helm.sh/release-namespace: jenkins
 ---
 apiVersion: rbac.authorization.k8s.io/v1
 kind: ClusterRole
```
That is probably necessary for any recent Helm and not specific to Docker
Destkop.

