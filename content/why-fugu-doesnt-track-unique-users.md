---
title: "Why Fugu doesn't track unique users"
type: standard
draft: false
---

Tracking unique users is the norm in the product analytics industry today. Tools like Mixpanel, Amplitude and Google Analytics track events based on unique users with personally identifiable information (PII) such as IP addresses by default. They allow you to store any PII freely. In their user interface, you can drill down to user profiles and see exactly who has done what over long periods of time.

This is not good.

That's why Fugu doesn't let you track unique users by design, and saving any PII to event property values is against our terms of service.

## Why is tracking unique users and PII bad for privacy?

I think it's obvious why storing PII is bad. Of course, you will need some PII for your app to work (such as an email address to create a user account), but you should make sure to only store this data if it's absolutely necessary (e.g., on your own server, to process payments), and not send that info out left and right to third parties.

Why tracking unique users is bad might be less obvious.

Tracking unique users means that anyone who has access to the tracking data can see what a specific user has done and when. Privacy is a [human right](https://www.un.org/en/about-us/universal-declaration-of-human-rights). It doesn't matter if you have anything to hide or not. Every person should have the right to not be tracked in a way that potentially violates their privacy.

We accept that Netflix of Spotify know exactly what we watched and what we listened to. Providing a service doesn't give companies the right to shit all over your privacy. They need to give their customers a way to opt out, or better yet, not store and analyze this kind of data in the first place.

## What about tracking anonymized unique users?

Still not a good idea. Even if you cryptographically hash a user's identifier (e.g., email, database ID), information will be tied to a unique, albeit anonymous, user. However, there are still ways to map this data to a specific person. For example, if you have access to the unique anonymous data set, and know that Peter performed event A at a specific point in time, you can map his unique anonymous identifier to all past and future events.

Another way to exploit anonymous data is to analyze the behavior, and assign a psychological profile to a specific user or groups of users. This is how microtargeting for online ads works today.

But even if your data isn't used in such a way - why should you accept that a company has the right to track everything you're doing?

As soon as this kind of data is stored, it can potentially be abused. On purpose, as described above, by accident (giving access to third parties), or by malign intent (data getting stolen).

Fugu's approach is simple: We don't store unique user data in the first place.

## Is it possible to gain enough user behavior insights without tracking unique users?

Yes, of course.

It might seem like you need fancy retention and cohort analyzes to build a successful tech product, but the reality is that you don't. Most of the value you will get from simply seeing how different parts and features of your product are used. You can even go further and track more detailed information for these events (called property values) without tracking unique users. For example, understanding how many times your users use feature A over feature B, and being able to segment it further by paid vs. free users, will already get you a ton of information.

Conversion funnels are another tool that will give you great insight and doesn't require tracking unique users. For example, it can help you understand where in your check-out flow potential customers drop off.

A retention analysis might give you some more insights, but that will be a small increment of insights compared to events and conversion funnels, and is not worth the huge privacy trade-offs you'll need to make.

Furthermore, adding more features and analyzes complicates the usage of an analytics software, which in turn decreases its usefulness.

At Fugu, we're committed to making a simple tool that lets you quickly get an overview of how people use your product without invading their privacy.

As The Notorious B.I.G put it: Mo data, mo problems.