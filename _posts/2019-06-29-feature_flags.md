---
layout: post
title: "Feature Flags: Part 1"
date: 2019-06-29T16:33:56-05:00
update: 2019-07-01T18:36:36-05:00
categories: [software engineering]
---
I've seen a lot more information about [Feature Flags](https://en.wikipedia.org/wiki/Feature_toggle) recently, so I decided to learn more about them and look at some related products.

# Feature Flags: What & Why?
First, a little context. In a nutshell, Feature Flags (which seems to be the name most people use to describe this) are used to turn a specific feature (or section of code) 'on' or 'off'. 

This is especially valuable if you're trying to work along the Continuous Integration/Development/Deployment (CI/CD) spectrum. In this context, you want new code integrated into your core code base as early as possible, not living in a separate feature branch.  As useful as feature branches are, the 'richer' that branch becomes, the larger/more complex it's eventual integration into your main code base becomes. And if you're trying to work along the CI/CD spectrum, you want to *minimize the size* & complexity of these merges or re-integrations by *maximizing their frequency*. That's where the 'Continuous' part comes from: that's the goal.

So, instead of having Work In Progress (WIP) branches for each feature, you can work on those features IN your main code base, but put them behind feature flags that you can turn on/off. This allows you to develop new features WHILE you also continuously integrate/deliver/deploy your code.

Another potential use case is where you're less concerned about CI/CD, but don't want the hassle of maintaining multiple versions of your software for different clients/environments/situations. In this case, you can have a single code base, with feature flags to differentiate between the various scenarios.

A third potential use case would be related to testing. Say you have functional tests you want to run on different versions of your software. You could try to use feature flags to decide which tests run against a specific version of your software. That's something I may be trying to figure out in the near future, so I'll have to get back to you on that.

#  Feature Flags: How?
That all sounds GREAT in theory. The problem comes in how you make it work. As your scenarios become more complex, managing the flags becomes more problematic. You can try to "roll your own" solution, but the complexities there are what often cause dev teams to NOT try feature flags.

The GOOD news: there are companies that have worked this out for you. In my next post, I'm going to look at one of these companies, [Launch Darkly](https://launchdarkly.com/).  I'm going to try their product and see if I can get it to work in a simple example.🤞🏾