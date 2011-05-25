---
layout: post
title: Patching dbext vim plugin to support Rails naming conventions
published: false
tags: 
- rails
- vim
- dbext
- patch
- convention
- sql
---

[dbext](http://www.vim.org/scripts/script.php?script_id=356) is an excellent vim plugin that allows you to execute SQL queries directly from vim. For example: execute `select * from ` &lt;word under cursor&gt;. When dbext is used with Rails there is a problem that you can work with some variation of table name like: UserRole, user\_role\_id, user\_role\_ids or user\_role, but still wants to use it in your database queries so that you won't type it manually.

<!--more-->

So, I made it to automatically convert word under cursor into a table name with the following configuration options:

    let g:dbext_table_names_number = 2 
        # 0 - disabled, 1 - singular, 2 - plural
    let g:dbext_table_names_case = 2 
        # 0 - disabled, 1 - camelcase, 2 - underscore

Also there is an option to automatically strip *_id* suffix from word to convert it to table name:

    let g:dbext_table_names_strip_id = 1

All staff in [my dbext fork](http://github.com/bogdan/dbext).
Also if you like this change - [support my pull request](https://github.com/zklinger/dbext/pull/1).

Now put your cursor on any variation above and run `:DBSelectFromTable` to get `select * from user_roles`.
Other commands are also patched. Please let me know if any bugs found.
