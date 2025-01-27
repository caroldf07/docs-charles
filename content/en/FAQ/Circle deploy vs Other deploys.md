---
title: Circle deploy vs Other deploys
weight: 93
description: >-
  In this section, you will find an explanation about the difference between
  circle deploy and other deployments methods.
---

---

## Circle deploy x Traditional deploy

In traditional deploys, it's common that the application has to pass into different environments until it gets to production. With Charles, the circle deploy system works only in the production environment. The release validation is fragmented according to selected circles, in other words, you can open gradually the access to your release to more and more circles.

![Process of traditional deploy ](/shared/deploy-tradicional%20%282%29.png)

![Process of circle deploy](/shared/deploy_em_circulos%20%283%29%20%281%29.png)

## Circle deploy x Blue-green deploys

At blue-green deployment, it's possible to create two identical environments in your infrastructure, but with different versions of an application implemented in each other. In this way, it's possible to test your hypothesis that, once confirmed, can be migrated from one version to another.

The main benefit is that the downtime is zero, which brings more safety for the transition process. Despite this, it represents a higher cost because this deployment demands double of infrastructure to be executed.

With Charles, the circle deploy offers to teams more confidence and agility on launching new versions, with zero downtime and no additional costs on infrastructure. Besides, it's possible to filter, through circles, which users will validate your new application version.

![Process of blue-green deploy](/shared/blue_green%20%281%29%20%281%29.png)

![Process of circle deploy](/shared/deploy_em_circulos%20%281%29%20%281%29.png)

## Circle deploy x Canary release

At canary release, it is done the gradual publishing of a software new version from routing within the infrastructure. As soon as the version is tested and it's more trustworthy, your access is expanded to more users from your base.

However, this technique doesn't have any strategy for choosing the users during this expansion. For this reason, it becomes more difficult to manage the existing versions of your system, which contributes to not working with many versions, generating limits of possibilities to test hypothesis.

With Charles, the circle deployment logic follows a pattern similar to parallel change. That means that, in the platform, you can also start opening the access to a release to a reduced number of users and go gradually expanding as soon as the system passes into tests.

The main difference of Charles is that, if you find any error or you have a hypothesis already validated, the reverse is easily done: you can take users off the circle or make deployment of another version with that group or even bring a version of your application to [**open sea**]({{< ref path="/key concepts.md" lang="en">}}), that is, to all the clients not in a Charle's circle.

![Process of Canary Release](/shared/deploy_em_circulos_x_canary_releases%20%282%29.png)

![Process of circle deploy](/shared/deploy_em_circulos%20%2810%29.png)
