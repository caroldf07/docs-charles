---
title: Overview
weight: 4
description: >-
  In this section, you will find more information about installing Charles.
---

---

## Components

CharlesCD's installation considers these **components**:

1. **Charles' architecture** specific modules; 
2. **Keycloak**, used for authentication and authorization;
3. A **PostgreSQL database** for backend modules \(`moove`, `circle-matcher`, `butler,` `villager` and `charlescd-compass`\) and Keycloak;
4. A **Redis**, to be used by `charlescd-circle-matcher`
5. By default, a module called `octopipe` is added to the installation. This is a native platform created by our team to make installation easier, without previous configurations. However, you can disable it in the installation files.

## Requirements

To install Charles will be necessary an environment with the following requisites: 

* [**Kubernetes**](https://kubernetes.io/docs/setup/).
* [**Istio**](https://istio.io/archive/) \(version =&gt; 1.7 and [**enabled sidecar injection**](https://istio.io/latest/docs/setup/additional-setup/sidecar-injection/#automatic-sidecar-injection) on the deploy namespace of your application\).
* [**Prometheus**](https://prometheus.io/docs/prometheus/latest/getting_started/)**,** in case you want to use [**metrics**](/reference/metrics/setting-up-your-metrics/) 
* [**Ingress**](https://github.com/kubernetes/ingress-nginx)

{{% alert color="warning" %}}
**What is Ingress?** It is an engine that exposes HTTP and HTTPS routes from outside the cluster to services within the cluster. You can find out more about it [**in the documentation**](https://kubernetes.io/docs/concepts/services-networking/ingress/#what-is-ingress). 

When you install Charles it comes with a default ingress, however, if you want to use your own, follow [**the steps to enable it**](/get-started/optional-configuration/configuring-your-ingress/).
{{% /alert %}}

## Resources 

The minimum resources considering only the installation of Charles are: 

* **Microk8s**: 2GB of RAM; 
* **Minikube**: 4GB of RAM. 
* **Cluster**: 2GB of RAM

## Next steps

In this section, you saw components, requirements, and resources to install Charles. To continue the installation, see: