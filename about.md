---
layout: page
title: What is Taskette?
sidebar_link: true
---

Scheduled tasks are a necessary part of applications. Some common examples might be:
* Sending an email _n_ days after a user signs up.
* Backing up databases or logs every night.
* Checking whether important servers are up or down, and reacting when they're down.

These tasks become important business logic components, and their execution needs to be guaranteed. As a business grows, so do its operations, and these tasks suddenly start taking on more and more work and need to scale.

---

Taskette was created out of a need for a reliable, scalable scheduled task system.

Taskette is created for developers and administrators who want to focus on writing business logic, and not writing cron statements and timers or managing machines. As Taskette is a completely managed system, it can often be more powerful than what's directly available to the engineers.

# Using Taskette

At this point, a few examples will probably demonstrate Taskette better than words can.

Let's take our 3 examples from above and implement them in Taskette.

## Sending an email _n_ days after a user signs up.

Here we've seen a basic example, where we request that our URL is called after 3 days. We've used a POST request with a JSON body. In 3 days, Taskette will call our URL with the correct parameters and we'll send that email.

## Backing up databases or logs every night.

Here, we've used an existing crontab expression to define a recurring task. This makes moving from cron to Taskette much easier. Simply put your task behind a URL and use the same cron expression.

## Checking whether important servers are up or down, and reacting when they're down.

This time, we've used Taskette's syntax for defining a recurring task (we could've used cron too). We've also created an alert to let us know when our response returns anything other than a 20x response. We'll receive an email when one of our services is down, and we'll be able to react accordingly.

# Taskette and URLs

At this point, you've probably noticed that we give Taskette a URL for each task that we schedule.

URLs are the entry point into your code. We don't have access to your services, your scripts, your databases. We just call a URL we some parameters at a certain point of time. The beauty of Taskette is its simplicity - you can put whatever you like behind the URL, meaning you can use Taskette for pretty much any piece of work.

Your existing tasks might not be accessible via URL, and our development team are always available to help you migrate easily and securely to use Taskette.

# Why Taskette ?

Scheduling work is not a new concept, but we're trying to make it better. We talk about other solutions and how they can be used here.

Here are a few reasons why Taskette is the right tool to use:

## Reliable

Taskette is built to guarantee task execution. We've taken the most reliable tools in the industry and built our system around them.

## Scalable

Taskette is built to handle billions of requests and we don't break a sweat if you're managing 5 or 5000 scheduled tasks.

We're built to call URLs. If your tasks start becoming heavier and need to be scaled across multiple machines, simply put a load balancer behind the URL you give to us.

We're working hard to ensure scaling your system is as easy as possible, keep tuned for more news!

## Secure

We don't know anything about your system or how you're going to respond to our calls.

All URLs given to Taskette need to be for domains validated by your administrator, ensuring that your endpoints are at risk to attack.

We also support several authentication methods to ensure your Taskette account is safe, and that your URLs are only called by us.

## Dynamic & Programmable

A cron system isn't dynamic. If you want to add a scheduled task based on a request, you'll need to manually add a new cron task. Imagine our previous example: sending an email to a user 3 days after they sign up. That's quite difficult to do with non-dynamic systems.

In Taskette, it's easy. From your application code you can make a call to Taskette and the job is created instantly.

## Stress-free

Cron requires servers. Even learning the crontab syntax can be an effort in itself. Debugigng failed tasks, ensuring that jobs are run on time. These are all problems that have been solved before and detract from building your application. We centralize all the best practices and provide a simple interface, meaning you spend less time debugging servers and more time writing code.

## Language Agnostic

We don't care what you behind your URL. It can be Node, Java, Go, Python, anything you like! Some tools will force you into their toolchains, meaning you have to rewrite application code. Not us.

## Measurable & Reactive

Equally important as the business logic is the measurability of that logic. This is actually quite hard to do with current solutions. We've built it in from the beginning.

You also want to know when jobs fail, or return strange values. We have a complete alerting suite to help with that.

# Getting Started

* Google Functions
* AWS
* Custom Application
* Coming from Cron