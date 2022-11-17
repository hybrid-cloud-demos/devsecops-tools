#devsecops-tools

Helm Charts to deploy devsecops tools onto OpenShift 4 cluster. The charts will create a buildConfig that will create an imagestream based off of the `tools` imagestream that already exists within the OpenShift cluster. 

When the build has completed an imagestream for:

- [cosign](https://github.com/sigstore/cosign)
- [rekor](https://github.com/sigstore/rekor)
- [roxctl](https://www.redhat.com/en/resources/advanced-cluster-security-for-kubernetes-datasheet)

Which can then be called by other services such as openshift-pipelines or kubernetes job/cronjobs.