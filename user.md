---
layout: concertina
title: NeoMutt - A User's View
---
# NeoMutt - A User's View

NeoMutt has many improvements over Mutt.
Below is a list of all the differences between Mutt and NeoMutt.

This guide is correct as of Mutt-1.8.3 and NeoMutt-20170609.
It is written for **users** of NeoMutt.
If you're a developer, see the [Developer's View](develnclude "rfc822.h").

## Removed from NeoMutt

NeoMutt wants to remain compatible with Mutt, but it also wants to improve the
user's experience.  To achieve this, NeoMutt has added many features to Mutt and
removed very little.

### Features

**`mutt_dotlock`** The only feature that has been removed from NeoMutt is
`mutt_dotlock`.  It was a primitive file-locking program which was needed when
Mutt was young and network filesystems weren't as reliable as they are now.

See also: [List of NeoMutt features](https://www.neomutt.org/feature.html)

### Variables

Two obsolete variables have been removed from NeoMutt.

- `dotlock_program` -- Command is obsolete
- `smime_sign_opaque_command` -- Variable wasn't used

There are 24 synonyms (aliases) for variables in NeoMutt
These old names haven't been in the documentation for over ten years.

| Obsolete Name            | Correct Name               |
| :----------------------- | :------------------------- |
| `edit_hdrs`              | `edit_headers`             |
| `envelope_from`          | `use_envelope_from`        |
| `forw_decode`            | `forward_decode`           |
| `forw_decrypt`           | `forward_decrypt`          |
| `forw_format`            | `forward_format`           |
| `forw_quote`             | `forward_quote`            |
| `hdr_format`             | `index_format`             |
| `indent_str`             | `indent_string`            |
| `mime_fwd`               | `mime_forward`             |
| `msg_format`             | `message_format`           |
| `pgp_autoencrypt`        | `crypt_autoencrypt`        |
| `pgp_autosign`           | `crypt_autosign`           |
| `pgp_auto_traditional`   | `pgp_replyinline`          |
| `pgp_create_traditional` | `pgp_autoinline`           |
| `pgp_replyencrypt`       | `crypt_replyencrypt`       |
| `pgp_replysign`          | `crypt_replysign`          |
| `pgp_replysignencrypted` | `crypt_replysignencrypted` |
| `pgp_verify_sig`         | `crypt_verify_sig`         |
| `post_indent_str`        | `post_indent_string`       |
| `print_cmd`              | `print_command`            |
| `smime_sign_as`          | `smime_default_key`        |
| `xterm_icon`             | `ts_icon_format`           |
| `xterm_set_titles`       | `ts_enabled`               |
| `xterm_title`            | `ts_status_format`         |

These synonyms are still accepted by NeoMutt, but they will soon be deprecated.
First there will be an announcement; then warning messages in NeoMutt; then
finally they will be removed.

**Please update your config.**

### Functions

No functions have been removed in NeoMutt.

### Commands

No commands have been removed in NeoMutt.

### Colours

No colours have been removed in NeoMutt.

## Changed in NeoMutt

NeoMutt is moving forward and some things are getting changed.

### Features

These six features have changed slightly -- they were adopted by upstream Mutt!

| Feature             | Description                                        | In NeoMutt  | In Mutt            |
| :------------------ | :------------------------------------------------- | :---------- | :----------------- |
| Sidebar             | Overview of mailboxes                              | 2016-03-07  | 2016-07-06 (1.6.2) |
| Trash Folder        | Automatically move deleted emails to a trash bin   | 2016-03-07  | 2016-08-18 (1.7.0) |
| TLS-SNI             | Negotiate with a server for a TLS/SSL certificate  | 2016-03-07  | 2017-04-12 (1.8.1) |
| Compressed Folders  | Read from/write to compressed mailboxes            | 2016-05-30  | 2016-12-04 (1.7.2) |
| Kyoto Cabinet       | Kyoto Cabinet backend for the header cache         | 2016-10-02  | 2017-04-12 (1.8.1) |
| LMDB                | LMDB backend for the header cache                  | 2016-07-23  | 2017-04-12 (1.8.1) |

Mutt now supports the same six header-cache backends, but there is one important
difference.  Mutt can only compile-in one backend: NeoMutt can have several
backends.  This allows distros to offer their users a choice.

### Variables

If you have upgraded from a very old version of NeoMutt, it might be necessary
to update some of your sidebar config.  The names were changed to better match
NeoMutt's other variables.

| Old Name               | New Name                |
| :--------------------- | :---------------------- |
| `sidebar_delim`        | `sidebar_divider_char`  |
| `sidebar_folderindent` | `sidebar_folder_indent` |
| `sidebar_indentstr`    | `sidebar_indent_string` |
| `sidebar_newmail_only` | `sidebar_new_mail_only` |
| `sidebar_shortpath`    | `sidebar_short_path`    |
| `sidebar_sort`         | `sidebar_sort_method`   |

### Functions

These very old sidebar functions were also renamed.

| Old Name              | New Name            |
| :-------------------- | :------------------ |
| `sidebar-scroll-down` | `sidebar-page-down` |
| `sidebar-scroll-up`   | `sidebar-page-up`   |

### Commands

No commands have been changed in NeoMutt.

### Colours

No colours have been removed in NeoMutt.

## Added to NeoMutt

### Features

These are the major features of NeoMutt that haven't been adopted by Mutt.

| Feature                  | Description                                                            | Since        | Status     |
| :----------------------- | :--------------------------------------------------------------------- | ------------ | ---------- |
| Attach Headers Color     | Color attachment headers using regexp, just like mail bodies           | 2016-09-10   | stable     |
| Compose to Sender        | Send new mail to the sender of the current mail                        | 2016-10-02   | stable     |
| Conditional Dates        | Use rules to choose date format                                        | 2016-03-07   | stable     |
| Encrypt-to-Self          | Save a self-encrypted copy of emails                                   | 2016-07-23   | stable     |
| Fmemopen                 | Replace some temporary files with memory buffers                       | 2016-03-07   | disabled   |
| Forgotten Attachment     | Alert user when (s)he forgets to attach a file to an outgoing email.   | 2016-09-10   | stable     |
| Global Hooks             | Define actions to run globally within Mutt                             | 2016-08-08   | stable     |
| Ifdef                    | Conditional config options                                             | 2016-03-07   | stable     |
| Index Color              | Custom rules for theming the email index                               | 2016-03-07   | stable     |
| Initials Expando         | Expando for author's initials                                          | 2016-03-07   | stable     |
| Keywords                 | Labels/Tagging for emails                                              | 2016-05-30   | stable     |
| Limit Current Thread     | Focus on one Email Thread                                              | 2016-03-28   | stable     |
| Multiple FCC             | Save multiple copies of outgoing mail                                  | 2016-08-08   | stable     |
| Nested If                | Allow complex nested conditions in format strings                      | 2016-03-07   | stable     |
| New Mail                 | Execute a command upon the receipt of new mail.                        | 2016-07-23   | stable     |
| NNTP                     | Talk to a Usenet news server                                           | 2016-05-30   | stable     |
| Notmuch                  | Email search engine                                                    | 2016-03-17   | stable     |
| Progress Bar             | Show a visual progress bar on slow operations                          | 2016-03-07   | stable     |
| Quasi-Delete             | Mark emails that should be hidden, but not deleted                     | 2016-03-07   | stable     |
| Reply With X-Original-To | Direct reply to email using X-Original-To header                       | 2016-09-10   | stable     |
| Sensible Browser         | Make the file browser behave                                           | 2016-09-10   | stable     |
| Skip Quoted              | Leave some context visible                                             | 2016-03-28   | stable     |
| Status Color             | Custom rules for theming the status bar                                | 2016-03-07   | stable     |

### Variables

    abort_noattach
    ask_follow_up
    ask_x_comment_to
    attach_keyword
    catchup_newsgroup
    collapse_all
    debug_file
    debug_level
    empty_subject
    flag_chars
    followup_to_poster
    forward_references
    from_chars
    group_index_format
    header_cache_backend
    header_cache_pagesize
    header_color_partial
    history_remove_dups
    inews
    keywords_legacy
    keywords_standard
    mime_subject
    newsgroups_charset
    newsrc
    news_cache_dir
    news_server
    new_mail_command
    nm_db_limit
    nm_default_uri
    nm_exclude_tags
    nm_hidden_tags
    nm_open_timeout
    nm_query_type
    nm_query_window_current_position
    nm_query_window_current_search
    nm_query_window_duration
    nm_query_window_timebase
    nm_record
    nm_record_tags
    nm_unread_tag
    nntp_authenticators
    nntp_context
    nntp_listgroup
    nntp_load_description
    nntp_pass
    nntp_poll
    nntp_user
    pgp_encrypt_self
    pgp_self_encrypt
    pgp_self_encrypt_as
    post_moderated
    reply_with_xorig
    save_unsubscribed
    show_multipart_alternative
    show_new_news
    show_only_unread
    sidebar_on_right
    skip_quoted_offset
    smime_encrypt_self
    smime_self_encrypt
    smime_self_encrypt_as
    ssl_verify_partial_chains
    vfolder_format
    virtual_spoolfile
    xlabel_delimiter
    x_comment_to

### Functions

### Commands
    finish
    ifdef
    ifndef
    lua
    lua-source
    shutdown-hook
    startup-hook
    tag-formats
    tag-transforms
    timeout-hook
    unvirtual-mailboxes
    virtual-mailboxes

### Colours
    attach_headers
    index_author
    index_collapsed
    index_date
    index_flags
    index_label
    index_number
    index_size
    index_subject
    index_tag
    index_tags
    progress
    sidebar_ordinary
