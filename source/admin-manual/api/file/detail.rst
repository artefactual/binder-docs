.. _api-file-detail:

File Detail
===========

.. http:get:: /api/file/(uuid)

   Returns a summary of a file given its UUID.

   **Example request**:

   .. sourcecode:: http

      GET /api/file/3fc23edf-6ef2-4ce7-b86d-dd9af1ad9ac6 HTTP/1.1
      Host: example.com

   **Example response**:

   .. sourcecode:: http

      HTTP/1.1 200 OK
      Content-Type: application/json

      {
          "id": 12345,
          "uuid": "3fc23edf-6ef2-4ce7-b86d-dd9af1ad9ac6",
          "slug": "foobar",
          "filename": "foobar.png",
          "media_type": {
            "id": 136,
            "name": "Image"
          },
          "mime_type": "image/png",
          "path": {
            "master": "http://example.com/uploads/r/null/1/2/12345/foobar.jpg",
            "thumbnail": "http://example.com/uploads/r/null/1/2/12345/foobar_142.jpg"
          },
          "process_history": {
            "WORK", "IN", "PROGRESS"
          }
      }

   :statuscode 200: no error
   :statuscode 404: there's no file


:ref:`Back to API documentation index <api>`