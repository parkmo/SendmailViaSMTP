README
=======

.. contents::

What is SendmailViaSMTP
-------------------------

SendmailViaSMTP is an easy used command line kit for sending mail via smtp server which can use in multiple platforms like linux, BSD, Windows etc. Like `msmtp <http://msmtp.sourceforge.net/>`_ but don't need compile and install in each machine. Just copy SendmailViaSMTP.py to any machine which had python installed.
SendmailViaSMTP is distributed under the BSD license.

Where is SendmailViaSMTP
--------------------------
* Origin-Homepage: http://www.himysql.com (Chinese)
* Origin-Source code: https://github.com/leopku/SendmailViaSMTP
* 2to3 and 3run tested code: https://github.com/parkmo/SendmailViaSMTP

Features
---------

* Accept data from pipe as email body.
* Tls support. This means we support sending mail using gmail.
* Multi recipient support.
* Multi system supported, like Linux, BSD, Windows etc.
* **NEW**: Attachments support(using -a/--attach option, see help message for more).
* log support. use --log option for debugging.

Requirements
-------------

* `python`_ 3.x (test on 3.9.2)

.. _python: http://www.python.org/

How to use SendmailViaSMTP
----------------------------

Download
~~~~~~~~~
#. Git clone(recommend)
    $git clone https://github.com/leopku/SendmailViaSMTP.git

#. Download 
    #. Dowload last source code zip/tar.gz package from http://github.com/leopku/SendmailViaSMTP/archives/master
    #. Download last package uploading by developer from http://github.com/leopku/SendmailViaSMTP/downloads

Run SendmailViaSMTP.py in terminal
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
#. pipe mode [#]_
    $echo "contents from pipe." | python SendmailViaSMTP.py --host="mail.domain.com" --from="myname@yourdomain.com" --to="friends1@domain1.com;friends2@domain.com" --user="myname@yourdomain.com" --password="p4word" --subject="mail title"

#. file mode
    $python SendmailViaSMTP.py --host="mail.domain.com" --from="myname@yourdomain.com" --to="friends1@domain1.com;friends2@domain.com" --user="myname@yourdomain.com" --password="p4word" --subject="mail title" --file="/path/to/file"
    
#. option mode
    $python SendmailViaSMTP.py --host="mail.domain.com" --from="myname@yourdomain.com" --to="friends1@domain1.com;friends2@domain.com" --user="myname@yourdomain.com" --password="p4word" --subject="mail title" --content="contents from option"
    
**NOTE:** The priority of three mode: pipe mode, file mode, option mode.
    
TODO
-----

.. [#] pipe mode is very useful while working with nagios etc.
