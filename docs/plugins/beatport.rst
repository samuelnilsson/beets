Beatport Plugin
===============

The ``beatport`` plugin adds support for querying the `Beatport`_ catalogue
during the autotagging process. This can potentially be helpful for users
whose collection includes a lot of diverse electronic music releases, for which
both MusicBrainz and (to a lesser degree) Discogs show no matches.

Installation
------------

To use the ``beatport`` plugin, first enable it in your configuration (see
:ref:`using-plugins`). Then, install the `requests`_ and `requests_oauthlib`_
libraries (which we need for querying and authorizing with the Beatport API)
by typing::

    pip install requests requests_oauthlib

You will also need to register for a `Beatport`_ account. The first time you
run the :ref:`import-cmd` command after enabling the plugin, it will ask you
to authorize with Beatport by visiting the site in a browser. On the site
you will be asked to enter your username and password to authorize beets
to query the Beatport API. You will then be displayed with a single line of
text that you should paste into your terminal. This will store the
authentication data for subsequent runs and you will not be required to
repeat the above steps.

Matches from Beatport should now show up alongside matches
from MusicBrainz and other sources.

If you have a Beatport ID or a URL for a release or track you want to tag, you
can just enter one of the two at the "enter Id" prompt in the importer.

.. _requests: https://docs.python-requests.org/en/latest/
.. _requests_oauthlib: https://github.com/requests/requests-oauthlib
.. _Beatport: https://beetport.com
