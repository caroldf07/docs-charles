---
title: Cd Configuration
weight: 51
description: 'In this section, you''ll find how to make the CD configuration'
---

---

## Why do you have to configure the CD? 

This configuration is necessary to point to Charles which CD tool you use to make deploys in your cluster. It is also important to mention that you have to provide your git repository token that contains the [**helm templates.** ](/get-started/creating-your-first-module/how-to-configure-chart-template/)

At this moment, Charles is able to use CharlesCD \(Octopipe\). 

{{% alert color="info" %}}
CharlesCD is always evolving, so there's a roadmap that is in constant update, which means that we're looking for more CD tools integrations.
{{% /alert %}}

## How to configure?

Charles uses a proper architecture for Continuous Deployment \(CD\) and that makes it fits in the environment chosen by you. These tools are used to run the Kubernetes manifestos on a configured cluster and to authenticate with a variety of cloud providers \(AWS, GCP, Azure\). 

To make this configuration, you will use CharlesCD. Now, it is necessary to fill some fields with the authentication for the cluster.

* **CharlesCD**: behind the scenes, there is a light and low-cost tool developed by Charles Team that does the deployment.

To register, follow the next steps: 

1. On Charles' homepage, select **Settings** in the lower-left corner;
2. Click on **Credentials;**
3. Click on **Add CD Configuration;**
4. Select the option **CharlesCD**, which will depend on which system you use. 

## Using CharlesCD

Fill the following fields:

1. **Name:** configuration name that it will be created; 
2. **Namespace:** defines the namespace that will be used on Kubernetes cluster deploys. You have to create your namespace, once Charles does not do it;
3. **Git provider**: defines the git provider to be used \(**GitHub** or **GitLab**\);
4. **Git token:** insert an authentication token that has access to the git repository where your [**Helm templates**](/get-started/creating-your-first-module/how-to-configure-chart-template/) are stored \(they will be used during the deployment of your [**application**](/get-started/creating-your-first-module/overview/)\). If your Git Provider is **GitHub**, "_repo_" permission is required. Otherwise, configure the accesses in **GitLab**: "API" and "_read\_repository_".
5. Select a **manager** to associate with the CD configuration. The options are **Default**, **EKS,** and **Others.**

### **Default**

This option must be used when the application’s cluster is the same where CharlesCD is installed. This way it is not necessary to create an extra authentication mechanism. 

### **EKS**

For a cluster managed by EKS \(Elastic Kubernetes Service\), you only have to select the option and fill the following fields:

1. **AWS SID:** Statement ID**;**
2. **AWS Secret:** Access key to EKS cluster; 
3. **AWS Region:** Region where the EKS cluster is installed; 
4. **AWS Cluster Name:** EKS’s cluster name.

### **Others**

For the other cloud providers, we use a simpler approach, that only a few _kubeconfig_ fields must be used. Here they are: 

1. **Host:** Cluster URL's access;
2. **Client Certificate:** _kubeconfig_ "client-certificate-data" field;
3. **Client Key:** _kubeconfig_  "client-key-data" field;
4. **CA Data:** _kubeconfig_  "certificate-authority-data" field.

All the information provided above is encrypted by Charles. Once this process is done, it is possible to associate the configuration in modules and after that deploy versions of them.