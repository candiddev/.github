---
author: Mike
date: 2023-09-17
description: Choosing a licensing model for your source code can be almost as difficult as writing code.
title: Navigating Software Licensing
type: blog
---

> **Obligatory legal disclaimer**:  This is not legal advice.  You should consult with a lawyer who specializes in software licensing and intellectual property before choosing a license.  They will help you choose a license that aligns to your goals.

You've just written a bunch of code, what next?  In most of the world, you've just created [Intellectual Property](https://en.wikipedia.org/wiki/Intellectual_property), an intangible creation that is wholly owned by you.  You have the __copyright__ to the code: only you can use or copy.

At this point, you could stick the code on GitHub and no one can legally do anything with it (though it won't stop folks from reading/forking/training their LLM on it...).  Your software is in the [No License](https://choosealicense.com/no-permission/) limbo: all rights are still reserved by the creator.

## Rights are Permissions

You need to grant rights to users for your source code.  Think of your source code like a file on your computer, and a software license like the permissions of that file.  By default, only you have permission for that file, and you have to explicitly grant access to other users, organizations, or everyone.

Unlike file permissions, software licenses can grant a wide array of permissions, conditions, and other legal mumbo jumbo.  They can be as long or short as necessary to explicitly grant the permissions you want.  Most folks typically pick a pre-canned license created by organizations like the GNU, Mozilla, MIT, or Apache.  Others create their own license and hope for the best.

## Choosing a License

Sites like [Choose a License](https://choosealicense.com/) can help you navigate some of the precanned licenses out there, but I feel this website and others try and push users unfairly towards permissive licensing like MIT.  It's "simple and permissive", and front and center on the page.  Lots of big companies refuse to use any software that isn't MIT (or BSD) licensed.  So why doesn't everyone just use MIT and call it a day?

**The rights you grant to your users and the conditions of those rights need to align to your goals**.  Choose a License asks you what your **current situation** is.  Instead, you should ask yourself, **what do I want my future situation to be**.  Because once you choose a license and publish code online with it, there's no going back.  You can relicense future work (in theory, need another blog post to discuss that can of worms), but the code you released will forever be covered under that license (unless the license had some kind of expiration, such as the [BSL](https://mariadb.com/bsl11/)).

## Licensing Outcomes

Lets explore some possible licensing scenarios to give you an idea of where choosing one license might lead:

### Source Available Licenses

Source available licenses are a broad category of licenses that have any conditions or restrictions preventing the free use of the software, such as the BSL, SPPL, or Elastic license.  Folks argue about semantics for source available licensing, but a good "is it source available" test is to ask yourself "can I unconditionally resell this source code?".  If the answer is no, then it's most likely a source available license.  Source available license restrictions typically aim to prevent the commercialization of source code by folks other than the creator.  Users may have some usage access, but source available licenses also encompass literal "view-only" source code licenses too.  This category should probably be broken out more in the future, but as of 2023 source available licenses are not very well received.

For you, the creator of the software, you will see whatever kind of benefit you want from using this license.  You will most likely be able to make money, possibly even be the sole beneficiary of that money.  Your license will prevent competitors from reselling your souce code, but it will not prevent them from attempting to replace your source available version with a more permissive version (such as Amazon Web Services creating OpenSearch as a FOSS replacement for Elastic's ElasticSearch).

Due to the license restrictions, you may find yourself with far fewer users than a permissive license.  Users may not feel comfortable using a source available license, or may not be able to without paying money.  You project will almost certainly not "top the star charts" on GitHub.  If your goal is to make a popular project, this probably isn't the license for you.

### Permissive Licenses

Choosing a permissive license like MIT is extremely common.  With this license, and others like Apache or BSD, your users can do whatever they want with the software as long as they distribute your copyright/LICENSE file with their software.  They can resell it, add it to new software, create private or public forks, basically every "permission checkbox" is ticked.

For you, the creator of the software, you will see no direct benefits from using this license.  Folks are not required to share their changes with you, forks can "take control" of your community, and you will receive no monetary or "reputational" compensation from folks using or selling your source code.  Big companies love MIT software for exactly this reason: it's free work for them.  Instead of having to write a library or a piece of code, they can use your code without paying you anything for it.

You may find work doing consulting or bug fixes for your code, possibly getting some donation/sponsorship income, but you will most likely find yourself like thousands of other open-source contributors with nothing to show for your work but issues and other demands of your users.  The number of folks (and organizations) who earn a living off of permissive licensing is small, because that's the point of a permissive license: you're giving away all of the rights unconditionally.  If your goal is to make money, this probably isn't the license for you.

### Copyleft Licenses

Sitting somewhere in the middle of source available licensing and permissive licensing is copyleft licensing.  And like Source Available licensing, copyleft licensing has a gamut of flavors.  The idea of "copyleft" is using copyright against others: if a piece of work incorporates a copyleft piece of work, the original piece of work may be required to change some or all of its licensing.  Copyleft licenses almost always grant the same kind of rights as permissive licenses, but with the additional copyleft requirements.

Copyleft licenses come in various forms:

- File-based, such as the Mozilla Public License (MPL), where all of the source code _files_ are copyleft.  All future work involving changes to those files must be covered under a similar license.  You could modify the files to include a new source code file--the file modifications would be copyleft, but the new source code file would not.
- Repository-based, such as the GNU Public License (GPL), where all of the code in the repository is copyleft, and any kind of linking or usage within your source code will require your source code to become GPL as well.

For you, the creator of the software, you may not see any direct benefits from using this license.  There will be some requirements to share changes, though not explicity with you (typically only "users", though you may be a user of a piece of work that derives from your source code), but forks can still happen, and you are not entitled to any compensation.  Big companies will not use your source code, as the infectious nature of the copyleft requirement would be too damaging for them (typically).

You will find yourself in a similar situation as the Permissive License, however one thing not commonly discussed online about copyleft licenses is the room for exemptions:  you still own the copyright, and you can absolutely relicense your code on an individual basis.  Companies hate copyleft licenses, but they could pay you to have your software relicensed as MIT for their usage.  This kind of licensing setup with exemptions is frowned upon, in my opinion, because it puts the power back in the creator's hand.  You are still creating a free, open-source software, but companies can no longer use it without contributing to the ecosystem or paying you (and sustaining the ecosystem).  If your goal is to build a community and make money, this might be a good license for you.

## Summary

After writing source code, choosing a license is by far the most important next step.  There are a lot of licenses to choose from, and a lot of opinions online on which one is the best to pick.  As a creator, it is up to you on which one to pick, and your choice should be based on your goals, not anyone elses.
