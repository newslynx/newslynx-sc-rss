
Sous Chefs
-------------
**newslynx-sc-rss** provides access to the following Sous Chefs

Ingest Articles from an RSS Feed
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Extracts articles from an RSS Feed.
-  This Sous Chef runs the python module ``newslynx_sc_rss.Article``.
-  API Slug: ``rss-feed-to-article``

Development
^^^^^^^^^^^

Pass runtime options to ``rss-feed-to-article`` and stream output.
**NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_rss/article.yaml option=value1

Alernatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_rss/article.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_rss/article.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=rss-feed-to-article **options

Alerternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=rss-feed-to-article --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alernatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options, ``rss-feed-to-article`` also
accepts the following

-  ``feed_url``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``url``



