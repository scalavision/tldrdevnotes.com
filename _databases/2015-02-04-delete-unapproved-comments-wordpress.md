---
layout: post
title: Delete ALL Unapproved comments in WordPress
permalink: wordpress-mysql-delete-unapproved-comments
tags:
- wordpress
- mysql
excerpt: How-to delete all unapproved WordPress comments in one go via PhpMyAdmin
---

Make a backup first before changing anything.

Go to PhpMyAdmin and select the comments table (usually `wp_comments`). Go to the SQL tab and run the following command.

```sql
DELETE FROM wp_comments WHERE comment_approved = 0
```

That's all. 