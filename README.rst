----------------------
PyCon Zimbabwe Website
----------------------

Repository for the source code of the PyConZim website.

===========
Development
===========

Point your web browser to the `PyConZim Website <https://github.com/PyZim/PyZim.github.io>`_ repository and tap the Fork button at top-right.

Then clone the source for your fork and add the upstream project as a Git remote:

Clone the repository::

     $ git clone --recurse-submodules https://github.com/YOUR-USERNAME/PyZim.github.io

     $ cd PyZim.github.io

Switch to the `Pelican` branch::

     $ git checkout Pelican 

Install dependencies::

     $ pip install -r requirements.txt

Run the devserver::

     $ pelican -dlr --port 8000

Now you can browse the website at `http://localhost:8000/`. To stop the server,
hit Ctl-C 

===============
Adding Features
===============

Create a topic branch for your fix or feature::

     $ git checkout -b name-of-your-fix-or-feature

-----------------------
Submitting your changes
-----------------------

Commit your changes and push your topic branch::

     $ git add .
     $ git commit -m "Your detailed description of your changes"
     $ git push origin name-of-your-fix-or-feature

Finally, browse to your repository fork on GitHub and submit a pull request.



==========
Deployment
==========

For deploying the website, the rendered HTML needs to be pushed to the `gh-pages`
branch. This can be done via the `Makefile` and the `ghp-import` script::

    $ pelican content -o output -s pelicanconf.py
    $ ghp-import output -b gh-pages
    $ git push origin gh-pages

The current version should be live now at https://pyconzim.co.zw/

=========================
Changing the HTML and CSS
=========================

The templates and css we are using are defined in the directory PyZim.github.io/event-agency-theme/. To change the css you can edit the stylesheet pyconzim.css located in Pyzim.github.io/event-agency-theme/static/css/pyconzim.css. The event-agency-theme is ported to `Pelican <https://docs.getpelican.com>`_ from `Startbootstrap's Agency Theme <https://startbootstrap.com/previews/agency>`_.  

