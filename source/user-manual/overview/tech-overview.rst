.. _tech-overview:

==================
Technical overview
==================

.. _Artefactual: http://www.artefactual.com/
.. _AtoM: https://www.accesstomemory.org/
.. _Archivematica: https://www.archivematica.org/
.. _MoMA: http://www.moma.org/

Binder has been created by leveraging existing functionality from AtoM_, and
adding new functionality on top of it.

.. image:: images/atom-binder.*
   :align: center
   :width: 80%
   :alt: Reusing AtoM as a basis for Binder

AtoM is comprised of:

* HTML pages served to a web browser from a web server (Nginx)
* A database on a database server (MySQL 5.1+)
* PHP (5.3.10+) and several PHP extensions, and the Symfony (1.4) framework
* Elasticsearch, a distributed search server based on Apache Lucene, which AtoM
  interacts with via a RESTful API

For more information, see the `AtoM documentation <https://www.accesstomemory.org/docs>`__.

Additional modules specific to Binder have been added via
`AngularJS <https://angularjs.org/>`__ (1.2) front-end pages, which Binder
communicates with via an HTTP API.

Binder-specific UI components, written in AngularJS, have been abstracted from
AtoM, which is currently used as a back-end dependency. This abstraction will
allow AtoM to be replaced in the future if desired, as Binder grows and the
need for a customized environment (e.g. a database, web server, and search
index specific to Binder) becomes more relevant.

Since Binder’s front-end consumes data via a RESTful API, it can be integrated
with other applications in the future with minimal structural changes. See the
:ref:`API documentation <api>` for more details.

:ref:`Back to top <tech-overview>`
