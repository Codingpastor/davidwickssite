---
title: "Archives"
description: "Every post published on this site, grouped by year."
date: 2025-04-15
layout: "archive"       # Uses layouts/_default/archive.html
slug: "archives"        # URL: /archives/
# Retired. This listed exactly the same posts as /posts/ ("Writing"), and with
# a post count well under one page of pagination the two could never differ.
# /posts/ is the canonical URL - post pages link back to it and it owns the
# RSS feed - so this is the one that goes. /archives/ now redirects to /posts/
# via an alias declared on content/posts/_index.md.
#
# Kept as a draft (unbuilt) pending confirmation to delete this file and
# layouts/_default/archive.html. The year-grouping layout is worth revisiting
# if the blog ever outgrows a single page.
draft: true
# NOTE: deliberately no `menu` entry here. The Archives link is defined once,
# in hugo.toml under [[menu.main]]. Setting it in both places put two Archives
# items in the nav.
---

Every post published on this site, newest first.

If you'd rather browse by topic, try the [categories](/categories/).
