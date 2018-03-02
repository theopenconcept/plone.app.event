plone.app.event
===============

Plone.app.event is the calendaring framework for Plone. It provides Dexterity behaviors and an Archetypes type, Timezone support, RFC5545 icalendar export, Recurrence support, event views and a lot more.

For a Dexterity event type using plone.app.event, use plone.app.contenttypes 1.1 or newer.

The complete documentation can be found on: https://ploneappevent.readthedocs.org



## Extended functionality from the open concept UG ##

With these changes to importer.py it's possible to fetch icalendar from ssl-secured webresource secured by auth digest on webservers side.
The new format of inputline is:

https://theopenconcept.de/ ... /cal.ics&<auth-domain>&<username>&<password>

obviously it's not possible to use any names or passwords that contain the '&' char as this simple patch only does a simple split('&') to separate the data-strings. Furthermore no checks other than formal adherence to URL naming rules.




Installation
------------

For Standalone installation follow the standard buildout procedure::

    $ virtualenv .
    $ ./bin/pip install -U zc.buildout setuptools pip
    $ ./bin/buildout

For Plone 4.3 do::

    $ ./bin/buildout -c buildout-43.cfg

Note, both commands will install a test and development environment.
