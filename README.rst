=====================
Make Heggedal website
=====================

We use `lektor <https://www.getlektor.com/>`_ to build our webite. Install lektor with::

    pip install lektor

Then build the site with::

    lektor build -O output

This will put everything into the `output` directory. From there you can copy it wherever you need.

Developers
==========

You can run an auto-reloading development server with::

    lektor serve

Deployment
==========

When you push to the master branch on github, we deploy it make-heggedal.no.

The site is currently served on netlify.