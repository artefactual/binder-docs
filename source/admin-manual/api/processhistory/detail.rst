.. _api-processhistory-detail:

Process History Detail
======================

.. http:get:: /api/processhistory/:id

   **Example request**:

   .. sourcecode:: http

      GET /api/processhistory/1984956 HTTP/1.1
      Host: example.com

   **Example response**:

   .. sourcecode:: http

      HTTP/1.1 200 OK
      Content-Type: application/json

      {
          "id": 1984956,
          "TMP": ["WORK", "IN", "PROGRESS"]
      }


   :reqheader Accept: accepted MIME types are :mimetype:`application/xml` and :mimetype:`application/json` (default)

   :resheader Content-Type: this depends on :http:header:`Accept` header of request

   :statuscode 200: no error
   :statuscode 404: there's no file


:ref:`Back to API documentation index <api>`