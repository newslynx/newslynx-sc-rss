
Sous Chefs
-------------
**newslynx-sc-rss** provides access to the following Sous Chefs

Ingest Articles from an RSS Feed
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Extracts articles from an RSS Feed.
-  This Sous Chef runs the python module
   ``newslynx_sc_rss.feed.Article``.
-  API Slug: ``rss-feed-to-article``

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_rss/feed_to_article.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=rss-feed-to-article **options

Alternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=rss-feed-to-article --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Development
^^^^^^^^^^^

Pass runtime options to ``rss-feed-to-article`` and stream output.
**NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_rss/feed_to_article.yaml option=value1

Alternatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_rss/feed_to_article.yaml --recipe=recipe.yaml

Options
^^^^^^^

In addition to default recipe options, ``rss-feed-to-article`` also
accepts the following

-  ``feed_url``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``url``



Google Alerts to Event
~~~~~~~~~~~~~~~~~~~~~~

-  Extracts events from a google alerts RSS feed.
-  This Sous Chef runs the python module
   ``newslynx_sc_rss.google_alerts.Events``.
-  API Slug: ``google-alert-to-event``

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_rss/google_alerts_to_event.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=google-alert-to-event **options

Alternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=google-alert-to-event --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Development
^^^^^^^^^^^

Pass runtime options to ``google-alert-to-event`` and stream output.
**NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_rss/google_alerts_to_event.yaml option=value1

Alternatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_rss/google_alerts_to_event.yaml --recipe=recipe.yaml

Options
^^^^^^^

In addition to default recipe options, ``google-alert-to-event`` also
accepts the following

-  ``feed_url``

   -  An RSS Feed URL for a Google Alert

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``url``

   -  More details on this option can be found
      `here <https://www.google.com/alerts>`__

-  ``must_link``

   -  Only create an event if there is a link to an existing content
      item.

   -  **Required**
   -  Should be rendered with a ``checkbox-single`` form.
   -  Choose from:

      -  ``False``

   -  Accepts inputs of type:

      -  ``boolean``

   -  Defaults to ``False``

-  ``event_status``

   -  Set the status of the resulting events. Choose from pending and
      approved. Defaults to pending.

   -  Should be rendered with a ``select`` form.
   -  Choose from:

      -  ``pending``
      -  ``approved``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``pending``

-  ``set_event_title``

   -  Set's the title of the resulting events. This can be a python
      format string which has access to all of an event's top-level
      keys: IE: "Content from {authors} at {created}."

   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``set_event_description``

   -  Set's the description of the output events. This can be a python
      format string which has access to all of an event's top-level
      keys: IE: "{title}."

   -  Should be rendered with a ``paragraph`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``set_event_tag_ids``

   -  A list of Tag IDs or slugs to automatically apply to events
      created by this recipe.

   -  Should be rendered with a ``checkbox`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``string``
      -  ``numeric``

   -  Defaults to ``[]``

-  ``set_event_content_items``

   -  A list of Content Item IDs and Titles to automatically apply to
      events created by this Recipe.

   -  Should be rendered with a ``search`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``json``

   -  Defaults to ``[]``



