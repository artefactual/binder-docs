.. _project-status:

======================
Current project status
======================

.. _Artefactual: http://www.artefactual.com/
.. _AtoM: https://www.accesstomemory.org/
.. _Archivematica: https://www.archivematica.org/
.. _MoMA: http://www.moma.org/
.. _TMS: http://www.gallerysystems.com/tms
.. _Elasticsearch: https://www.elastic.co/
.. _Vagrant: https://www.vagrantup.com/

Binder's original development was planned by MoMA_ and Artefactual_ in the
second half of 2013, and carried out from January to June 2014. In the initial
development, the application was created specifically for MoMA's primary use
cases, and made to work within MoMA's environment, including existing
applications already in use at the Museum, such as TMS_. MoMA currently uses
Binder in production within the Musuem.

Now that the initial development goals have been achieved, both Artefactual and
MoMA hope to expand the utility of the project by open sourcing its code and
making it available to other developers. We believe that Binder can help a broad
set of cultural heritage institutions achieve their long-term preservation goals,
and would like to see the Binder project develop into a full-fledged,
production-ready, open-source application with its own vibrant community.

In late 2014 and early 2015, initial steps to generalize and open-source the code
have been undertaken. MoMA was using a custom branch of both Archivematica_ and
AtoM_, and the hope is to get Binder functioning/integrated with the most recent
public releases of Archivematica and AtoM. **Work remains before the application
can be used in its present form, however.**

The main two issues can be summed up as such:

* The initial development was done using Elasticsearch_ 0.9 as the search index.
  The most recent AtoM releases use ES 1.3, but the upgrade means that some
  sections of the code will need to be tested and rewritten before the application
  is usable.
* MoMA had a custom Archivematica branch that could upload to Binder, but we'd
  like to make Binder work with the most recent public Archivematica release. In
  the long-term, this means adding an "Upload to Binder" option into the general
  Archivematica project. Another goal would be the ability to create new Artwork
  records via the user interface (rather than via Archivematica upload on the
  custom Binder branch, and metadata pulled from TMS) - then the usual method
  of inputting a slug into Archivematica could be used. An even simpler short-term
  workaround might be to create a command-line script that will generate a new
  artwork record for upload using the existing slug method in Archivematica. Since
  none of these workarounds have yet been implemented, at present there is no
  simple way to attach AIPs and DIPs from Archivematica to nodes in Binder.

We have created some installation instructions using Vagrant_, so that
developers can work with the code. Note that this will **not** lead to a
functioning installation at present - but we hope that community developers
might help us tackle some of the isues outlined by our developers as part of
the installation notes. See them here:

* https://gist.github.com/sevein/e0b1d036721435add3cd

Resolving these issues are our first priority, so we can better expose the
project to the cultural heritage community. We have also listed some long-term
project ideas, on the following page, :ref:`project-goals`.

Why not help us out? If you are a developer interested in working with Binder,
check out our `GitHub repository <https://github.com/artefactual/binder>`__, and
feel free to post questions in our
`User Forum <https://groups.google.com/forum/#!forum/binder-repository>`__.
