---
layout: post
title:  "Sync Starred Results to Twitter Lists"
date:   2017-02-24 14:40:00 -0800
categories: features
---

ScoutZen lets you sync your scout results to Twitter lists. This feature
has been getting increasingly popular, and we have made some changes to
make it efficient while giving users full control over what gets synced.
The improved sync policy enables several interesting use cases, which
we will describe in more detail below.

## Introducing Starred Results

As you might have noticed, we have spruced up the scout results page.
Instead of one profile per row, on desktop and tablet form factors, each
row displays three mini-card style profiles.

![Profile Cards](/assets/three-cards-row.png)

This new approach lets us achieve several UX goals: 

1. __Increased information density__. Everything about a particular profile
   can be taken in quickly in a few hundred pixels, without having to
   scan the whole screen. 
1. __Layout consistency__. Profile fields are always in expected places
   without wrapping or extending horizontally or vertically, despite
   variations in field length or their absence. 
1. __Logical grouping__. Links for profile lookup and follow are
   adjacent, while ScoutZen actions are clustered together. This also
   benefits from and contributes to layout consistency.
1. __More available actions__. Finally, this redesign allows us to
   place two new features within easy access: a) Display matching tweets
   and b) Star selected results.

### Mark With a Star 

Each profile includes a star as the first action at the top right. Use
it to mark people who you consider important or want to find easily. An
already starred profile simply shows an orange star instead of a
clickable button. These "starred results" can be easily accessed by
selecting "Starred" from the Actions dropdown.

Within the Starred results listing, any item can be "Unstarred" if you
no longer want it marked special. 

### Making Lists

Starring results is thus a great way to organize people for follow-up.
In effect, you can conveniently build a list within the scout results,
with a quick indication (star) that you have done so. 

So its only natural that you would want to turn these starred results in
to a Twitter list. If you have not done so yet, check out our [primer on
Twitter lists and their many benefits][sztwlist].

## Syncing to Twitter List

ScoutZen has long had [support for syncing results to Twitter
lists][prevsync]. As described earlier, syncing results to Twitter lets
you see the list timeline and tweets in your favorite Twitter client.

Setting up the sync is easy, either via scout settings, or directly from
the starred results page. 

![Sync Settings](/assets/sync-settings.png)

As before, start by providing the Twitter list name. If the list does
not exist, it is created automatically. Newly created lists can be
specified to be public or private as appropriate. The sync can be
temporarily disabled, but generally you would start by checking
"Enable Sync" and save the settings.

ScoutZen will then schedule an initial sync in the background. This will
create the list and add previously starred results as members. After
that, any starred items will be quickly and incrementally added to the
Twitter list. Conversely, unstarred items will be removed from the
Twitter list. 

### Sync Policies

1. If the specified Twitter list does not exist, it is created.
1. If the Twitter list exists, its attributes are not changed. 
1. After finding or creating the Twitter list, ScoutZen tracks the list
   by its list id. You are free to rename the list on Twitter, and
   ScoutZen will update its name to reflect the change. 
1. If you change the Twitter list name via ScoutZen sync settings, it
   does not rename the existing list. Rather, it finds or creates a
   Twitter list with the new name.
1. During initial sync, pre-existing members of a Twitter list are not
   purged. The sync will add starred results to the Twitter list.
1. Members are only removed from Twitter list if they are Unstarred in
   ScoutZen.
1. The sync is subject to rate limits and undocumented throttling. A
   large initial sync might take several days to get all members added. 

With these policies, it is possible for multiple scouts to sync to one
Twitter list. Starred items from all the different scouts will be added
to the list. Unstarred items will be removed, provided they are not
starred in other scouts syncing to the same list. 

Of course, as before, every scout can list to its own Twitter list. The
list can be changed at any point, in which case the new list will be
initialized with all previously starred results.

### One more thing...

For search scouts, you can view the tweet which led to the match and
inclusion within the scout results. 

![See Matching Tweet](/assets/see-tweet.png)

We believe these changes will let you curate Twitter list members more
effectively, while being selective and increasing awareness. In
particular, you can star results in conjunction with the search and sort
features. For example, find people with a keyword, sort them by number of
followers, review their profile at a glance and star them. Its easy to
star hundreds of items within a few minutes, while gleaning a lot of
understanding about the results.

Syncing to Twitter lists is just one more way ScoutZen can help you with
marketing and outreach. Stay tuned for more news on this and other
features!

[sztwlist]: /twitter/export/list/2017/02/01/twitter-list-export.html
[prevsync]: /scoutzen-news/twitter-lists/2016/08/01/twitter-list-sync.html
[searchsort]: /twitter/bio/search/2016/10/17/search-sort-tools.html

