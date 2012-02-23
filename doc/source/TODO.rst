######
TODO
######

how it works
============

load arbitrary 'plugins' (from a directory) on start.
the plugins have Python code to be triggered by a button with their name.

Also, they log (w/ timestamp) different actions:

    * service information (start/end of action)
    * what they do
    * raw technical information

callbacks
=========

plugin
-------

    * `button_name(locale=IGNORED)` // locale is ignored in first versions
    * several `info()`, `tooltip()`, whatever
    * `start(done_callback)`
    * `abort()` // should cleanup what can be cleaned
    * `status()` // I'm not so sure it's needed

later on, the plugin may come with fields (that come with type, default values and validation)

host app
--------

   * dynamic `done()`, that is handled to the plugin when started
   * `*_msg(...)` where * is a message type (no so sure)

info transmission
==================

save to file
---------

send mail
---------

send to server
--------------
