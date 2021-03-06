Changelog
=========


v0.5.0 (2014-12-01)
-------------------

- Updated ``Meta*`` model classes based on changes to Yummly API. Thanks flyingfrog81_!


v0.4.1 (2014-11-22)
-------------------

- Fix indentation issue in models.py. Thanks fredthekid_!


v0.4.0 (2013-09-10)
-------------------

-  Saner defaults for API data attributes
-  Use ``**kargs`` in model class ``__init__``s to avoid duplication
   of defaults/assignments
-  Use ``kargs.get()`` for API data attributes that may or may not be
   available to avoid key errors


v0.3.6 (2013-04-02)
-------------------

-  Fetch recipe ``yield`` keyword attribute safely from response since
   it's not guaranteed to be present
-  Supply defaults for ``recipe.nutritionEstimates``, ``recipe.images``,
   and ``recipe.yields``
-  Ensure ``totalTime`` and ``totalTimeInSeconds`` are set to ``0`` when
   falsey


v0.3.5 (2013-03-12)
-------------------

-  Change default value for ``Recipe.totalTimeInSeconds`` to ``0``:
   mirror default returned by search results
-  Change default value for ``SearchMatch.sourceDisplayName`` to ``''``:
   field not guaranteed to exist in return


v0.3.4 (2013-02-03)
-------------------

-  Handle top-level keys that are not always present in Yummly
   responses.
-  Provide default values for ``Recipe`` fields: ``rating=0``,
   ``flavors={}``, ``totalTime=0``, ``totalTimeInSeconds=''``,
   ``numberOfServings=0``, ``yields=''``, ``attributes={}``.
-  Assert that ``Client`` ``timeout`` parameter is >= 0.
-  Assert that ``Client`` ``retries`` parameter is >= 0 and an integer.


v0.3.3 (2013-02-02)
-------------------

-  Added ``retries`` parameter to ``Client`` which sets the number of
   additional requests to make after a Yummly timeout. Default is ``0``.


v0.3.0 (2013-01-26)
-------------------

-  Created ``Client`` class for handling API account configuration and
   request retrieval. Previously, these functions were handled in module
   functions.
-  Created new model classes for API return data.
-  Added ``Client.metadata`` function for fetching from Yummly's
   metadata endpoint.


v0.2.0 (2013-01-14)
-------------------

-  Added support for additional search parameters supported by Yummly.
   Previously only supported ``q``, ``maxResult``, and ``start``.


v0.1.0 (2013-01-13)
-------------------

-  Initial release.


.. _fredthekid: https://github.com/fredthekid
.. _flyingfrog81: https://github.com/flyingfrog81
