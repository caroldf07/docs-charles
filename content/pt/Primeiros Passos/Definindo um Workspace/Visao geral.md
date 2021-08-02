---
title: Visão Geral
weight: 20
description: Esta seção descreve como você deve configurar seu workspace dentro do Charles.
---

---

O workspace permite que você segmente o uso do CharlesCD dentro da sua empresa ou do seu time. Com ele se define as **permissões personalizadas dos usuários**, o que garante mais segurança para o seu projeto.

{{% alert color="info" %}}
Com apenas uma instalação, vários times podem utilizar o Charles com configurações distintas ou, se preferir, criar um workspace para representar diferentes ambientes de desenvolvimento como, por exemplo, homologação, produção, etc. 
{{% /alert %}}

### **Configurações do workspace**

Cada workspace possui as seguintes configurações:

* Definição dos acessos e [**permissões dos grupos de usuários**.](/pt/referência/grupo-de-usuários/)
* Cadastros de credenciais do [**Git**]()**,** [**Docker Registry**](/pt/primeiros-passos/definindo-um-workspace/docker-registry/) e de [**Continuous Deployment \(CD\)**](/pt/referência/preparando-o-seu-deploy/).
* Personalização do [**Circle Matcher**](/pt/referência/circle-matcher/).
* Registro do [**Provedor de Métricas**](/pt/primeiros-passos/definindo-um-workspace/adicionando-o-datasource/) das suas aplicações.

![Configura&#xE7;&#xE3;o de workspace](/shared/defining-workspace.png)

{{% alert color="warning" %}}
A criação do workspace pode ser feita apenas pelo usuário **root**. Entretanto, o preenchimento das configurações podem também ser feitas pelos usuários associados ao workspace com perfil de **mantenedor**.
{{% /alert %}}

### **Como obter o identificador do meu workspace?**

Assim que seu workspace é criado, mesmo sem a definição das configurações, ele já possui um identificador único. 

Para obter essa informação, selecione o workspace desejado e, no menu à esquerda, clique em **Copy ID**:

![](/shared/workspace_copyid%20%281%29.gif)