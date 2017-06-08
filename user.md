# NeoMutt - A User's View

If you're a developer, see the [Developer's View](devel.md).

## Removed

features

configure

variables
    smime_sign_opaque_command

functions

commands

colours

## Changed

features

configure

variables
    Old Name              New Name
    $sidebar_delim        $sidebar_divider_char
    $sidebar_folderindent $sidebar_folder_indent
    $sidebar_indentstr    $sidebar_indent_string
    $sidebar_newmail_only $sidebar_new_mail_only
    $sidebar_shortpath    $sidebar_short_path
    $sidebar_sort         $sidebar_sort_method

functions
    Old Name              New Name
    <sidebar-scroll-down> <sidebar-page-down>
    <sidebar-scroll-up>   <sidebar-page-up>

commands

colours

## Added

features
    Attach Headers Color     Color attachment headers using regexp, just like mail bodies         2016-09-10 stable
    Compose to Sender        Send new mail to the sender of the current mail                      2016-10-02 stable
    Compressed Folders       Read from/write to compressed mailboxes                              2016-05-30 stable
    Conditional Dates        Use rules to choose date format                                      2016-03-07 stable
    Encrypt-to-Self          Save a self-encrypted copy of emails                                 2016-07-23 stable
    Fmemopen                 Replace some temporary files with memory buffers                     2016-03-07 disabled
    Forgotten Attachment     Alert user when (s)he forgets to attach a file to an outgoing email. 2016-09-10 stable
    Global Hooks             Define actions to run globally within Mutt                           2016-08-08 stable
    Ifdef                    Conditional config options                                           2016-03-07 stable
    Index Color              Custom rules for theming the email index                             2016-03-07 stable
    Initials Expando         Expando for author's initials                                        2016-03-07 stable
    Keywords                 Labels/Tagging for emails                                            2016-05-30 stable
    Kyoto Cabinet            Kyoto Cabinet backend for the header cache                           2016-10-02 stable
    Limit Current Thread     Focus on one Email Thread                                            2016-03-28 stable
    LMDB                     LMDB backend for the header cache                                    2016-07-23 stable
    Multiple FCC             Save multiple copies of outgoing mail                                2016-08-08 stable
    Nested If                Allow complex nested conditions in format strings                    2016-03-07 stable
    New Mail                 Execute a command upon the receipt of new mail.                      2016-07-23 stable
    NNTP                     Talk to a Usenet news server                                         2016-05-30 stable
    Notmuch                  Email search engine                                                  2016-03-17 stable
    Progress Bar             Show a visual progress bar on slow operations                        2016-03-07 stable
    Quasi-Delete             Mark emails that should be hidden, but not deleted                   2016-03-07 stable
    Reply With X-Original-To Direct reply to email using X-Original-To header                     2016-09-10 stable
    Sensible Browser         Make the file browser behave                                         2016-09-10 stable
    Sidebar                  Overview of mailboxes                                                2016-03-07 stable
    Skip Quoted              Leave some context visible                                           2016-03-28 stable
    Status Color             Custom rules for theming the status bar                              2016-03-07 stable
    TLS-SNI                  Negotiate with a server for a TLS/SSL certificate                    2016-03-07 stable
    Trash Folder             Automatically move deleted emails to a trash bin                     2016-03-07 stable 

configure

variables
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

functions

commands
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

colours
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
