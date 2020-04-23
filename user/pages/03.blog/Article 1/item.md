---
title: 'Deploying a secure Grav CMS on DigitalOcean'
published: true
date: '22-04-2020 16:12'
---

Grav is a modern flat-file CMS that lets you a great looking CMS up and running in no time and you don’t have to be a CMS expert to do it.

Grav is easy and with a decent markdown editor almost anyone can create great looking CMSes with it. But it is a different story when it comes to host them esp. on VPSes such as DigitalOcean, Vultr, Linode, OVH, AWS etc. You not only have to understand how to spin off a robust server but also have to worry about how to make it secure. And that’s the easiest part!

Even if you have a secure server running, how do you make your website secure? Of course, encrypting it with SSL/TLS certificates! But they are neither cheap nor easy to set up.

Even if you thought that these are just one-time thing you have to do and spent a few hours getting everything properly configured, you still have to worry about deployments.

Grav comes with an optional admin plugin that allows you to quickly create contents and perform other admin tasks, just like good old WordPress. But you most probably want to write the contents locally, play with new plugins locally, proof-read, make sure everything is great to go and only then sync them all. You for sure don’t want to make changes to your live CMS on the fly.

Making sure you have all the above concerns adequately addressed and created an environment to painlessly deploy your CMS, is going to cost you hours if not days. And then you still have to worry about whether you configured everything correctly or not. Scary isn’t it?

But, fear not! Cleaver is here to rescue you from spending your valuable hours on something you are not good at and don’t even care — being a DevOps!

With Cleaver, you can have a robust and secure Grav CMS running in about 5 minutes! Let’s see how easy it is to do it.

## Step 1: Adding an API key of your server provider

Cleaver currently supports 📖 DigitalOcean and 📖 Vultr. Go to your server provider’s dashboard and copy the API key to Cleaver.

Follow these quick steps:
* 🎬 [DigitalOcean](https://www.youtube.com/watch?v=9EKtO_KfQvc)
* 🎬[Vultr](https://www.youtube.com/watch?v=x80xhiAS7Ro)