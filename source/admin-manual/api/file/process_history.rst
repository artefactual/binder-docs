.. _api-file-process_history:

File Process History
====================

.. http:get:: /api/file/(uuid)/processhistory

   Returns a summary of the process history of a file given its UUID.

   **Example request**:

   .. sourcecode:: http

      GET /api/file/3fc23edf-6ef2-4ce7-b86d-dd9af1ad9ac6/processhistory HTTP/1.1
      Host: example.com

   **Example response**:

   .. sourcecode:: http

      HTTP/1.1 200 OK
      Content-Type: application/json

      {
        "WORK", "IN", "PROGRESS"
      }

   :statuscode 200: no error
   :statuscode 404: there's no file


:ref:`Back to API documentation index <api>`