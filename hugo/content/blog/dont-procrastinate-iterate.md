---
author: Mike
date: 2023-09-04
description: Getting to a definition of done is hard, especially when there's a lot of work to do.
title: Don't Procrastinate, Iterate
type: blog
---

Developing software can be hard, especially when you're developing something new.  The anxiety over creating new code causes a lot of folks in the industry to get the opposite of tunnel vision, **forest vision**: even though they're only supposed to be working on a tree, all they see is the forest of additional stuff that needs to happen.  And it's overwhelming, like staring into the abyss.  This anxiety causes procrastination of varying degrees, and if you're not careful, it will severely impact your work performance and mental health.

## Types of Procrastination

**Delays in work can still look like work**.  The worst part is it ends up being the wrong kind of work, dutifully toiled, ultimately wasted.  It's long weekends, late hours of soul crushing work because you've fallen too far down a procrastination hole and can't see the light anymore.  Below I list a few of the scenarios I've encountered personally and while working with other teams, and further down I provide some tips on how to avoid them.

### Scope Creep

You're working on a well-defined feature request, and someone adds an additional requirement after work has been started.  Or you go to get clarification on a requirement and it blows up into a much bigger requirement.  The scope of your original issue explodes, but your deadline most likely didn't change.

### Future Thinking

While working on a feature request, you try practicing your ability to predict the future: if this features does X, surely it should probably do Y too.  Or you bang out a new app, admin interface, or tool, only to realize no one asked for it, no one wants it, and you either acknowledge you wasted a bunch of time for maybe a learning opportunity or you try and evangelize the use of it through some kind of career impacting crusade.  You built it after all, someone will find it useful too, even if you have to force them to use it!

### Premature Optimizations

This is similar to future thinking.  You start adding abstractions where there shouldn't be any yet, or you start performance tuning before you know the usage pattern.  You've satisfied the original requirements, but it's not quite "perfect" yet, and what's a few days of additional DRYing mean in the scheme of things?  You'll probably never get to touch this code again, some junior will start working on it after it's merged, or it's not up to the standards in your head.

## Avoiding Procrastination

A lot of software developers think requirements are there for the stakeholders to micromanage what you deliver.  The reality is, the requirements are there for your benefit.  They are the exact amount of functionality you are required to do.  It's to your benefit to get these requirements as specific, detailed, and micromanaged as possible.  Because the requirements are all that matters, and they will ground you when you get into your head too much.

As developers, we need to focus on the **definition of done** only.  If something that wasn't an original requirement comes up, or if you think of a whiz bang new feature or optimization, **create a new issue**.  These distractions will ruin your definition of done, and cause **you** nothing but misery.  If these are a requirement for the work you need to do, pause the current issue and start working on the new issue you opened--switch your definition of done to it.

### Ship Small Things Frequently

The easiest way to force yourself towards a definition of done is to ship small things frequently.  See if you can ship each requirement as an individual pull request, for instance, as that is a nice, clean boundary of work.  No one likes reviewing a massive pull request, and keeping things small and focused helps you and the reviewer understand the work that needs to be done and what was produced to satisfy that requirement.

### Embrace Iteration

By focusing on the requirements and shipping them frequently, you begin to embrace iteration.  This is a something a lot of other professions do not have the benefit of doing.  As developers, we can tap a few keys and rewrite ancient lines of code.  Code is never set in stone, it's meant to change and evolve.  Your codebase will never be complete, it will always be in a constant form of iteration.  Don't worry about perfecting that feature, just get it in your users hands so you can get their feedback.  You can optimize later, you can abstract it later, all that matters is getting real world feedback on what you did.

## Summary

Avoid getting trapped in your head and spending hours working on things that aren't important by focusing on what is actually required to deliver the functionality to your users.  Continue to iterate on that, **after it has been shipped**.  In the future, I'll discuss how to make iteration easy and safe, as well as how I approach tackling starting a new project from scratch.
