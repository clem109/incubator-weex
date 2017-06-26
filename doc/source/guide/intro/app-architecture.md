---
title: Mobile App Architecture
type: guide
order: 4.5
version: 2.1
---

# Mobile App Architecture

## Today's Mobile App

Let's talk about what we think a mobile app should be.

### Mobile App Needs Parallel Development

Nowadays, all mobile app teams require the ability to develop in parallel. When a mobile app keeps growing, supporting large-scale parallel development must become a priority. Otherwise, it's very easy to cause bottleneck's in application performance.

### Mobile App Needs to be Dynamic

Today the development of mobile apps is not very lightweight. It is slow in iteration, release, distribution and online bugfixing. The size of the package of an app is growing fast too. All of this is not suitable for this mobile internet age. Mobile apps need to be dynamic which is out of the cumbersome process of version deployment and distribution.

### Mobile App Needs Open Interconnection

Today in your phone, things are hard to connect and share between different apps. They need some containers with common standard and specs to be shared with each other.

## Our Thinking of Mobile App

We think a dynamic, parallel development supported, standardized mobile app should be like this:

```
|------|------|------|------| |-----|
| page | page | page | page | | api |
|------|------|------|------| | api |
| page | page | page | page | | api |
|------|------|------|------| | api |
| page | page | page | page | | api |
|---------------------------| | api |
|           router          | | api |
|---------------------------| |-----|
```

* Pages: A whole mobile app should be divided into several mobile pages. Each page has its own "URL".
* Router: All the mobile pages above will be connected with a router. Navigators or tab bars perform this job.
* Features: All kinds of APIs or services provided from the device. Every mobile page could use these features as they like.

So before you build your mobile app, make sure you know how many mobile pages your mobile app has and what they are. How do they connect with each other. Give each mobile page a URL and sort out all the APIs and services your mobile app needs.

Then create the pages and develop, debug and deploy them using Weex.

**Links**

* [Mobile page architecture](./page-architecture.html)

If you have built a complete mobile app already and just want to start using Weex to rebuild parts of these pages, that's absolutely no problem. Because Weex is just an SDK to build mobile pages which can coexist very well with other native views or hybrid pages.

If the feature of WeexSDK is limited to your mobile app. You can extend your own components and modules. It requires some native development knowledge. But with our efforts on delivering more and more features, we believe this part of job will be getting simpler and simpler.

**Links**

* [Extend to iOS](../../references/advanced/extend-to-ios.html)
* [Extend to Android](../../references/advanced/extend-to-android.html)
