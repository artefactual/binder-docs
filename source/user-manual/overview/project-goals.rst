.. _project-goals:

========================================
Project goals: Binder's long-term vision
========================================

.. _Artefactual: http://www.artefactual.com/
.. _AtoM: https://www.accesstomemory.org/
.. _Archivematica: https://www.archivematica.org/
.. _MoMA: http://www.moma.org/
.. _TMS: http://www.gallerysystems.com/tms
.. _CollectionSpace:
.. _Hydra: http://projecthydra.org/
.. _Islandora: http://islandora.ca/
.. _BitCurator: http://www.bitcurator.net/

Artefactual_ believes that Binder can help cultural institutions meet the
challenges of long-term preservation by providing access to metadata
(technical, administrative, descriptive, and preservation) that is critical in
informing digital preservation policy and practice.

We hope to see the Binder project grow, and are interested in partnering with
other cultural heritage institutions looking to solve similar challenges.
Below are some of the priority goals we see for the project as it develops:

.. _goals-generalization:

Generalize to support a broad set of use cases
==============================================

Binder was originally developed to help MoMA_ meet its goals implementing
standards-informed, best-practice digital preservation policies and practices.
As such, in its present form the application is not ready for broad use in other
institutional settings without further development.

Our first development goal is to generalize the application, so it can easily
be used to support a broad set of use cases and institutional practices out of
the box. In any future development project, we hope to build this kind of
generalization into the work carried out.

.. _goals-custom-environment:

Remove AtoM as a dependency for Binder
======================================

In the initial development of Binder, the app was built by leveraging existing
AtoM_ functionality and adding new features via
`AngularJS <https://angularjs.org/>`__ (1.2) front-end pages, which Binder
communicates with via an HTTP API. See the :ref:`tech-overview` for more
information.

The use of AtoM as a backend dependency was a development strategy necessary
to meet the desired goals with the resources available. As the project grows,
we hope to see Binder gain its own stack (database, web server, search index,
etc) tailored specifically to the goals of the project. This will not only
improve the long-term maintainability of the project, it will also improve
Binder's scalability and, by implementing a common data model already in use
by other open-source tools, help to support better interoperability and
integration with existing resources used by the cultural heritage community.

.. _goals-integration:

Integrate with more existing open-source tools
==============================================

Binder’s strength is in its ability to pull data from several disparate
applications used in preservation and conservation, and bring that information
together into a user-friendly interface. As the project develops, we would
like to see this approach maintained and expanded, so that Binder will be able
to communicate with a wide source of existing open source preservation tools,
including Islandora_, Hydra_, BitCurator_, and more. Integration with
CollectionSpace_ and other open source alternatives to TMS_ are also high on our
priority list. In general, Artefactual prefers to collaborate with and
participate in many of the exciting community development efforts already
underway, rather than compete by duplicating the functionality of existing
projects in novel ways.

.. _goals-preserve-binder-data:

Implement standards-based preservation of Binder data
=====================================================

At present, many of the complex relationships that can be created and managed
in Binder are only preserved in the MySQL database that Binder inherits from
AtoM_. We would like to see those relationships - between AIPs, artworks,
components, and supporting technologies - preserved in a standards-based way.
This could mean greater integration with Archivematica_, to allow for AIP
re-ingest or versioning, and/or the creation of Archival Information Collections
(AICs) designed to preserve relationships between preserved objects and
packages in an OAIS-compliant manner.

Further descriptive metatada import/export functionality should also be
considered to support the management of descriptive and technical metadata,
the documentation of process history, provenance, and more. Existing linked
data ontologies should be explored for their utlity in both preservation and
interoperability.

Artefactual_ has always aimed to support standards-based description and
preservation via its AtoM_ and Archivematica_ projects - we look forward to
continuing and broadening this work via the Binder project.

.. _goals-new-tools:

Develop new tools, reports, and visualizations
==============================================

Binder's strength is in the access to collections data and metadata that it
provides, and as the project grows, we hope to enhance the utility of the
application by expanding these capabilities to support more use cases and
functions. Below are a few areas where we are excited to consider how best to
enhance Binder.

Reports
-------

Presently, Binder includes a number of reports that can be generated by
repository managers, including reports on fixity, ingest, download, significant
properties, and more. Reports can be viewed in HTML tables via the user interface,
or downloaded in CSV format.

Adding further configuration options to existing reports, as well as expanding
the number and kind of reports available, are both prime goals for Binder as the
application grows.

Dashboard
---------

Binder's dashboard currently includes a number of widgets providing analytics
on collection size, growth, character, and activity. Making these widgets
configurable, adding further options, and allowing users to better interact
with the data displayed (including the ability to download and reuse it) would
vastly increase the utility of the Binder dashboard across a broad set of use
cases.

Context browser
---------------

One of Binder's most striking features is the context browser, available on
Artwork records. Built using the `D3 <http://d3js.org/>`__ library, it provides
users with a graphical user interface to create and manage complex relationships
between a work, its components, related AIPs, and the supporting technologies
required for ongoing preservation and access. By providing this information
visually, repository managers have a powerful and intuitive way to explore and
maintain collections data.

With the context browser, we have only begun to scratch the surface of what is
possible. We see great potential for optimizing and enhancing the existing
functionality, to provide repository managers with better and more intuitive
tools. Adding the ability to view the current tree in different ways could also
open up support for other kinds of cultural heritage data, including trees
with large hierarchical structures, such as those found in archival description.

Further views could also be added to the context browser - here are but a few
possibilities:

* **AIP view:** shift the context browser's focus from artworks to AIPs, and
  use the tree to display and manage contained directories, files, objects,
  as well as related supporting technology and component nodes. Submit changes
  back to Archivematica_ for AIP versioning and/or re-ingest.
* **Relationships view:** view and manage relationships between one work in
  the collection and others.
* **Taxonomy manager:** visualize and manage linked data ontologies and
  taxonomical hierarchies; manage relationships between a term and other node
  types in the repository.

---------------------------------------------

The goals and ideas outlined above are not exhaustive - they represent some of
the possibilities that have arisen during the development of Binder, and areas
which we see as important to consider for the long-term utility of the project.

Have you got other ideas? Why not start a discussion in our
`User Forum <https://groups.google.com/forum/#!forum/binder-repository>`__? If
you're a developer testing out Binder locally and would like to contribute code,
we love pull requests! Check out our Github repository here:

* https://github.com/artefactual/binder

If you are interested in discussing Binder development with Artefactual,
please feel free to contact us at info@artefactual.com

:ref:`Back to top <project-goals>`
