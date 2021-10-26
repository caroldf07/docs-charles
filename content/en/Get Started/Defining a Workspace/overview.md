---
title: Overview
weight: 21
---

---

The workspace allows you to segment CharlesCD's use in your team, defining **personalized users' permissions** that will assure safety to your project.

{{% alert color="info" %}}
You need only one installation, and the teams will be able to use Charles with different configurations, or you may create a workspace to represent different development environments, such as staging, production, etc.
{{% /alert %}}

### Workspace configuration

Each workspace has the following configurations:

* Access control and **user groups permissions**;
* **Git,** [**Docker Registry**](https://docs.charlescd.io/get-started/defining-a-workspace/docker-registry) and [**Continuous Deployment \(CD\)**;](https://docs.charlescd.io/reference/cd-configuration)
* [**Circle Matcher**](https://docs.charlescd.io/reference/circle-matcher);
* [**Metrics provider**](https://docs.charlescd.io/reference/metrics). 

![](//defining-workspace%20%281%29.png)

{{% alert color="warning" %}}
The **root** user gives you permission to create a workspace. However, users with **mantainer** profile are able to configure with the necessary information as well.
{{% /alert %}}

### How to get an identifier on my workspace?  <a id="como-obter-o-identificador-do-meu-workspace"></a>

Once your workspace is created, even without the configuration definitions**,** it already has a single identifier. 

To get this information, select the workspace you want, and then on the left menu, click on **Copy ID.**

![](//workspace_copyid%20%282%29.gif)