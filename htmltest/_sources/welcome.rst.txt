Nutanix Marvellous Workshop
===========================

In this workshop you'll learn new exciting content.

Open up this RST file to reveal the syntax and parameters of the example sections below.

Section 1 - Genius
+++++++++
Wouldn't it be good to show something in *italics*? Well, that was straightforward.

How about something in **bold**? Couldn't be more straightforward than that.

Spacing is important in Restructured Text so you may see errors simply because of space indents and tabs, or forgotten a closing **asterix**.

Also, if you want text to stÂart on a new line then make sure you leave a blank line after the last paragraph.

RAW HTML code can be included if necessary.

.. raw:: html

  <strong><font color="red">Something important because it's in red!</font></strong><font color="blue"> Less exciting because it's in blue :-)</font><br><br>

Here's a nice way to make a ``command instruction`` stand out.

|

An additional library is defined in the **conf.py** file to make special characters available, for example:

:fa:`bars` To show bars

:fa:`check` To show a tick

:fa:`square-o` To show a selection box

:fa:`arrow-left` To show a left-arrow

:fa:`arrow-right` To show a right-arrow

:fa:`arrow-up` To show a up-arrow

:fa:`arrow-down` To show a down-arrow

|

How about a nice checklist?

|o| Make the trainer a hot drink

|x| Ask questions

|x| Tidy away classroom when finished


Section 2 - Power
+++++++++
A description of something that would be benefit from a bullet list:

-   Item 1

-   Item 2

-   Item 3

Numbered bullets can have their place too:

#.   Item 1

#.   Item 2

#.   Item 3


Well, that was easy.

Section 3
+++++++++
At times you may want to point out something of note, an advisory or need something that simply stands out.

.. note:: Please ensure you've installed the correct version of blah before proceeding.

.. seealso:: There's another page you can click for more information.

.. warning:: A little more emphasis using this.


Quite simple when you know the syntax.

Section 4
+++++++++
It's time to include a graphic. This could be from screenshots you've been gathering or maybe you'd like to share something inspirational to liven the workshop up. Either way it's quite simple.

.. note:: Make sure you copy the image into the directory (or Folder for you Windows people) of your local repository, perhaps use a sub-directory called **images** too.

.. figure:: images/se-bootcamp-motivate.png

This will display the image in its native resolution so it may be worth checking the dimensions and reducing down if necessary. As you can see this is large :fa:`frown-o`.

If you'd like to constrain the image width then additional height and width parameters can be included in the RST file, you can specify one or both. See the source of this file and look for the `width` parameter.

.. image:: /images/se-bootcamp-how-logo.png
 :width: 250

The image insert isn't too complicated.

Section 5
+++++++++
Online materials invariably require URLs to be included and to keep the flow of your text it's sensible to include a hyperlinked word or phrase rather than dump in a string of messy text 200+ characters long.

In my example here I'm suggesting to `click here`_ to see the latest information about the topic I'm talking about. In the source code notice the use of the underscore.

.. _click here: http://my.nutanix.com/

You may want to embed a link to a Google Sheet as you may have seen in recent New Hire Training. Again, this uses RAW HTML and an iframe.

.. raw:: html

   <iframe src="https://docs.google.com/spreadsheets/d/1I7eLudDdxvKQDYvTzLFAXVQaGFYUl4LSVFJDuKx0lEI/edit?usp=sharing" style="position: relative; height: 400px; width: 98%; border: none"></iframe>


Section 6
+++++++++
Inserting code examples may be required especially if you would the content to look exact, here's an example taken from a Calm Workshop:


.. code-block:: bash

     #!/bin/bash
     set -ex
     # -*- Install httpd and php
     sudo yum update -y
     sudo yum -y install epel-release
     sudo rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm
     sudo yum install -y httpd php56w php56w-mysql

     echo "<IfModule mod_dir.c>
             DirectoryIndex index.php index.html index.cgi index.pl index.php index.xhtml index.htm
     </IfModule>" | sudo tee /etc/httpd/conf.modules.d/dir.conf

     echo "<?php
     phpinfo();
     ?>" | sudo tee /var/www/html/info.php
     sudo systemctl restart httpd
     sudo systemctl enable httpd





That covers many of the basics.
