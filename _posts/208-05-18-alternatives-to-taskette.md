---
title: Alternatives to Taskette
---

Scheduling work is not a new concept, but we're trying to make it better. Here's some other solutions you can use, and how they compare against Taskette.

## cron

cron is vanilla - it's the classic, but it's starting to feel dated. You won't find anything more battle-tested than cron, and it does its job well. However, when we look at how computing has changed in the past decade (cloud, distributed, horizontal scaling), it needs an update.

We understand that cron's syntax is globally recognized, that's why Taskette fully supports cron syntax. On top of that, you'll be getting the following things that cron doesn't offer:

* Managed service, you don't have to keep track of your cron machine. If you're in the cloud, you don't have to provision and manage a VM just for your cron tasks
* Built in task reporting, notifications, and alerts
* Horizontal scalability (and reliability across multiple machines)
* Durability (don't restart your cron server!)
* Dynamic tasks. Remember that cron needs to be statically defined on the machine. How would you send an email to a use 3 days after they signed up using cron? It's possible, but much more difficult.

## Building your own scheduler
* Language specific
## Azure Scheduler
## Amazon SWF
## Amazon Lambda using cron
## Google Functions using cron
## Chronos

# Why Taskette ?

* Using it in the Cloud.
* No more management of cron machines and job
* REporting on repeated tasks
* Scalable tasks
* Dynamic tasks

# Getting Started

* Google Functions
* AWS
* Custom Application
* Coming from Cron


posts
dynamic cron with other tools
cron with google cloud functions