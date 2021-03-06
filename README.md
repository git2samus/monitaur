Monitaur
========

A bash-ful way of monitoring web services.

vr 0.1

Installation
------------

1. Create a **.monitaur** folder in the home directory of 
   the user running monitaur.
2. Create a **urls** file in **.monitaur** with a new-line delimited list of
   the urls that you care about.
3. Create an **emails** file in **.monitaur** with a new-line delimited list
   of people who care about the urls you care about.
4. Create a **/var/log/monitaur** folder owned by the user running monitaur,
   for storing logs.
5. Add monitaur to the **bin** folder of your choosing, or set it up with cron.

Description
-----------

This program attempts to read a **urls** file in the **$HOME** directory of the user
executing it, and sends an HTTP request to urls contained therein, generating a log
file of responses.

If it discovers problems (no response, 4xx, 5xx, redirect response) this
program will then attempt to read an **emails** file in the **$HOME** directory
of the user executing it, and send emails to those addresses.  The emails will 
contain the log file's contents, thus appropriating the email owners'
attention to potentially misbehaving urls.

Issues
------

Please let me know via 
[Github's issue tracker](https://github.com/spacez320/monitaur/issues).

Development
-----------

This script was a learning experience.  Just saying.

Note that in the future I'll make this more a legitimate Linux program.  
I'll set up a make file or something.  Yeah, that's what I'll do; make a 
make file.  Or maybe I'll just go learn piano.

I was going to make this a daemon, because I wanted to write a daemon,
but then I realized that I'd have to call this program monitaurd.

License
-------

License GPLv3: GNU GPL version 3, 
[http://gnu.org/licenses/gpl.html](http://gnu.org/licenses/gpl.html).

Ths is free and open source software, you are free to modify and                                                                                                                    
redistribute it, but you must include this license.                                                                                                                                  
                                                                                                                                                                                     
There is no warranty for use of this software, to the extent permitted                                                                                                               
by law.                                                                
