---
title: Arbitrary merge testing with Perforce
featured: images/no_image.png
layout: post
comments: true
---


Working with [Paul Hammant](http://paulhammant.com) to build [Configuration-as-code](http://paulhammant.com/categories.html#configuration_as_code) system for [HedgeServ](https://www.hedgeserv.com/).

[Arbitary merge testing](https://github.com/ajaygautam/arbitary_merge_testing)

[Perforce setup helpers](https://github.com/paul-hammant/fast_perforce_setup)

This is part of a system to prove suitability of a version control system as backing store for a configuraton as code implementation.

This is line or para 2


asdaf


<p>Testing merges with Perforce</p>
<p>Work in progress...</p>

Create a DevBase branch with a config file
Create a UatBase branch - from the dev branch
Make mods to Dev, merge each to Uat
Verify Dev and Uat are in sync (nothing to merge. No ghost merges)
Create 5 clients. Make Uat and Prod branches for each
====> Every week - add new client - migrate from Uat and create prod
Week 1 - Make changes to dev. Merge all to Uat
Week 2 - Make changes to dev. Merge all to Uat
Verify dev and uat are "in sync"
Roll out all changes to all client's uat and prod
Verify dev and uat are "in sync"
Week 3 - Make changes to dev. Merge all to Uat
Week 4 - Make changes to dev. Merge all to Uat
Verify dev and uat are "in sync"
Roll out all changes to even indexed client's uat and prod
Week 5 - Make changes to dev. Merge all to Uat
Week 6 - Make changes to dev. Merge all to Uat
Verify dev and uat are "in sync"
Roll out all changes to odd indexed client's uat and prod
Week 7 - Make changes to dev. Merge all to Uat
Week 8 - Make changes to dev. Merge all to Uat
Verify dev and uat are "in sync"
Roll out all changes to all client's uat and prod
Verify dev and uat are "in sync"
Make a change in one client (random indexed) prod file
Merge change to client's uat
Merge change to uat base
Merge change to dev base
Start from week 1
Run the above 500 times


Automated test to perform merges across branches (Dev -> Uat -> Each client’s Uat -> Each client’s Prod)
Merge “back-the-chain” from a random client Prod all the way to Dev, and merge to all clients Prod env.
Started 7 days / 166 hours ago (still running): Created almost 1200 “client environments” 524,000+ commits (~3156 commits per hour) All files are currently in sync
