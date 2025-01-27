---
title: Releases
weight: 70
description: 'In this section, you will find more information about releases on Charles.'
---

---

Releases are application versions. It is different from other ways of deployment that a release generally goes through lots of environments until they reach production. However, with CharlesCD it is possible that the same release will be published for different [**circles**]({{< ref path="/Reference/Circles.md" lang="en">}}).

## **How to create releases with Charles?**

See how to create releases with Charles:

1. Existing images on docker registry.

This one offers the flexibility needed if you want cases in which the generation of artifacts or the development process is apart from CharlesCD.

### **Releases through existing images on configured Docker Registry**

To create a release without using the hypothesis board, it is necessary that the Docker images are already available on your [**configured registry**]({{< ref path="/Get Started/Defining a Workspace/Docker registry.md" lang="en">}}) for the module. If this requirement is done, just click on the [**circles**]({{< ref path="/Reference/Circles.md" lang="en">}}) **'** option on Charles' menu and select the circle for a release deployment to be created.

If you are creating the circle at this moment, click on **Insert release** and then Create release. If the circle is already created, click on **Override release** and then **Create release**.

On the release creation screen, fill in the name and select one module and its component. On the field beside, all available images on that component will be listed on the registry. Select one and, if it's necessary, add more modules to the release, clicking on **Add module** and repeat the previous process. When all your modules are registered, click on **deploy**.

![Exemple of release creation by Registry images](/shared/releases-por-meio-de-imagens-existentes%20%281%29%20%281%29.gif)

After deploying this new release, it will be available to use in other circles, just look into the '**Search for existing releases'** option.
