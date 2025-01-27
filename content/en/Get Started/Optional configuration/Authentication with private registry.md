---
title: Authentication with private registry
weight: 13
description: >-
  In this section, you will find more information about authentication with a
  private registry.
---

---

## **Why do you need to authenticate?**

Authentication is required if you use a private registry. This way, the cluster will be able to communicate with your registry to pull the images.

## **How do you authenticate?**

Kubernetes cluster uses a type of docker-registry **Secret** to authenticate the registry container. You have to generate it. 

{{% alert color="info" %}}
 For more information on how to generate the Secret that will be applied in your cluster, [**check out the Kubernetes documentation**](https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/). 
{{% /alert %}}

Once you generate the secret, it will look like this:

```text
apiVersion: v1
data:
  .dockerconfigjson: <<your value>>
kind: Secret
metadata:
  name: <<registry-name>>
type: kubernetes.io/dockerconfigjson
```

After this, you'll need to apply this information in the namespace where your applications will be deployed by Charles:

```text
kubectl -n your-namespace apply secret-registry.yaml
```

After completing these steps, your cluster will be able to maintain communication with the registry.
