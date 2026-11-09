=====================
Make Heggedal website
=====================

We use `Lektor <https://www.getlektor.com/>`_ to build our website.
Install `uv <https://docs.astral.sh/uv/getting-started/installation/>`_,
then build the site with::

    uvx lektor build -O output

This will put everything into the `output` directory. From there you can copy it wherever you need.

Developers
==========

You can run an auto-reloading development server with::

    uvx lektor serve

``uvx`` installs Lektor in an isolated tool environment; no project virtual
environment, ``pyproject.toml``, or lockfile is needed.

Deployment
==========

The workflow in ``.github/workflows/pages.yml`` builds the site and deploys
``output`` to GitHub Pages on pushes to ``master``. It can also be run manually
from the Actions tab on ``master``.

In the GitHub repository's Settings > Pages, select **GitHub Actions** as the
build and deployment source before the first deployment.

To use ``make-heggedal.no``, configure it as the custom domain in Settings >
Pages and update its DNS records to point to GitHub Pages. Remove the old
Netlify DNS records when switching hosts. Without a custom domain, the site
also works at the repository's default GitHub Pages URL.
