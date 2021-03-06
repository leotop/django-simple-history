Changes
=======

tip (unreleased)
----------------
- Add support for Django 1.8+
- Deprecated use of ``CustomForeignKeyField`` (to be removed)

1.5.4 (2015-01-03)
------------------
- Fix a bug when models have a ``ForeignKey`` with ``primary_key=True``
- Do NOT delete the history elements when a user is deleted.
- Add support for ``latest``

1.5.3 (2014-11-18)
------------------
- Fix migrations while using ``order_with_respsect_to`` (gh-140)
- Fix migrations using south
- Allow history accessor class to be overridden in ``register()``

1.5.2 (2014-10-15)
------------------
- Additional fix for migrations (gh-128)

1.5.1 (2014-10-13)
------------------
- Removed some incompatibilities with non-default admin sites (gh-92)
- Fixed error caused by ``HistoryRequestMiddleware`` during anonymous requests (gh-115 fixes gh-114)
- Added workaround for clashing related historical accessors on User (gh-121)
- Added support for MongoDB AutoField (gh-125)
- Fixed CustomForeignKeyField errors with 1.7 migrations (gh-126 fixes gh-124)

1.5.0 (2014-08-17)
------------------
- Extended availability of the ``as_of`` method to models as well as instances.
- Allow ``history_user`` on historical objects to be set by middleware.
- Fixed error that occurs when a foreign key is designated using just the name of the model.
- Drop Django 1.3 support

1.4.0 (2014-06-29)
------------------
- Fixed error that occurs when models have a foreign key pointing to a one to one field.
- Fix bug when model verbose_name uses unicode (gh-76)
- Allow non-integer foreign keys
- Allow foreign keys referencing the name of the model as a string
- Added the ability to specify a custom ``history_date``
- Note that ``simple_history`` should be added to ``INSTALLED_APPS`` (gh-94 fixes gh-69)
- Properly handle primary key escaping in admin URLs (gh-96 fixes gh-81)
- Add support for new app loading (Django 1.7+)
- Allow specifying custom base classes for historical models (gh-98)

1.3.0 (2013-05-17)
------------------

- Fixed bug when using ``django-simple-history`` on nested models package
- Allow history table to be formatted correctly with ``django-admin-bootstrap``
- Disallow calling ``simple_history.register`` twice on the same model
- Added Python 3 support
- Added support for custom user model (Django 1.5+)

1.2.3 (2013-04-22)
------------------

- Fixed packaging bug: added admin template files to PyPI package

1.2.1 (2013-04-22)
------------------

- Added tests
- Added history view/revert feature in admin interface
- Various fixes and improvements

Oct 22, 2010
------------

- Merged setup.py from Klaas van Schelven - Thanks!

Feb 21, 2010
------------

- Initial project creation, with changes to support ForeignKey relations.
