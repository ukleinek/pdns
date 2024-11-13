Random Backend
==============

.. deprecated:: 4.6.0
  This backend has been removed in 4.6.0

* Native: Yes
* Primary: No
* Secondary: No
* Producer: No
* Consumer: No
* Autosecondary: No
* DNS Update: No
* DNSSEC: Yes, no key storage
* Disabled data: No
* Comments: No
* API: ???
* Multiple instances: ???
* Zone caching: No
* Module name: built in
* Launch: ``random``

This is a very silly backend which is discussed in the :doc:`Backends
writer's guide <../appendices/backend-writers-guide>`.
as a demonstration on how to write a PowerDNS backend.

This backend knows about only one hostname, and only about its IP
address at that. With every query, a new random IP address is generated.

It only makes sense to load the random backend in combination with a
regular backend. This can be done by prepending it to the
:ref:`setting-launch` instruction, such as
``launch=random,gmysql``.

Configuration Parameters
------------------------

.. _setting-random-hostname:

``random-hostname``
~~~~~~~~~~~~~~~~~~~

-  String

Hostname for which to supply a random IP address.
