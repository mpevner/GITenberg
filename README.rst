Project Gutenberg Stats
=======================

Estimated 1.6 million files
Reported 650 GB total
~40,000 + books

Links to:  `Home Page`_ - `Book Repositories`_ - Issues_

.. _Home Page: http://gitenberg.github.io
.. _Book Repositories: https://github.com/GITenberg/repositories
.. _Issues: https://github.com/sethwoodworth/GITenberg/issues

How are we getting the files?
=============================

::

    rsync -rvhz --progress --partial ftp...

Each repo should...
===================

+ metadata.yml
  + author
  + title
  + publishing info
  + provinence
+ book_name.{rst|tei|txt}
  + book text in a master source format
+ license.txt
  + PG license information
  + transcriber, converter credits
+ README.rst
  + generic GITenburg info
  + generic PG info
  + book specific info
  + desc and links to toolchains
  + desc and links to generated versions for ebook readers

Smart comments:
===============

Convert all files to UTF-8
https://groups.google.com/forum/?fromgroups#!topic/prj-alexandria/VhKbMyH9kcA


File formats:
=============

A list of file formats and their freqency is in the docs folder, generated via:

::

    find -type f|rev|cut -d\. -f1|grep -v "/" |rev|sort -f|uniq -c|sort -nr

.tei
~~~~

a master format
http://www.tei-c.org/Tools/Stylesheets/
http://code.google.com/p/hrit/source/browse/rst2xml-tei.py?repo=tei-rest

.rst
~~~~

a master format
Research toolchain for rst >> whatever

dp rst manual http://pgrst.pglaf.org/publish/181/181-h.html

Future
------

+ http://armypubs.army.mil/doctrine/
