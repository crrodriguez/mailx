project('mailx', 'c',
  version : '12.6',
  default_options : ['warning_level=2'])

openssl_dep = dependency('openssl', version : '>=1.1.1')

glib_dep = dependency('glib-2.0')

# MIT Kerberos 5 GSSAPI support, does not currently work
gss_dep = dependency('mit-krb5-gssapi', required : false)

executable('mailx',
           'cache.c',
           'imap_search.c',
           'lzw.c',
           'maildir.c',
           'pop3.c',
           'ssl.c',
           'thread.c',
           'version.c',
           'cmd2.c',
           'cmdtab.c',
           'dotlock.c',
           'fio.c',
           'head.c',
           'imap.c',
           'lex.c',
           'names.c',
           'popen.c',
           'send.c',
           'smtp.c',
           'temp.c',
           'v7.local.c',
           'main.c',
           'junk.c',
           'macro.c',
           'openssl.c',
           'aux.c',
           'base64.c',
           'cmd1.c',
           'cmd3.c',
           'collect.c',
           'edit.c',
           'getname.c',
           'imap_gssapi.c',
           'list.c',
           'mime.c',
           'quit.c',
           'sendout.c',
           'strings.c',
           'tty.c',
           'vars.c',
           install : true, dependencies: [openssl_dep, gss_dep, glib_dep], gnu_symbol_visibility: 'hidden')

install_man('mailx.1')
