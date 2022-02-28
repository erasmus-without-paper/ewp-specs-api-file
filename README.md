EWP File API
============

* [What is the status of this document?][statuses]
* [See the index of all other EWP Specifications][develhub]


Summary
-------

This document describes the **File API**. This API allows partners to share files securely.


Request method
--------------

 * Requests MUST be made with HTTP GET method.


Request parameters
------------------

### `file_id` (required)

An identifier of a file the client requests.

Clients may retrieve proper file identifiers from other EWP APIs (like [Outgoing Mobilities API][omobilities-spec]).
Servers MUST be able to accept all file IDs shared with the caller through EWP APIs.


Security
--------

This version of this API uses [standard EWP Authentication and Security, Version 2][sec-v2].
Server implementers choose which security methods they support by declaring them in their Manifest API entry.


Permissions
-----------

Files should only be shared with those callers who have previously been provided with the file ID.


Handling of invalid parameters
------------------------------

 * General [error handling rules][error-handling] apply.


Response
--------

Servers MUST respond with the requested file.

Servers SHOULD return proper `Content-Type` header.

Servers SHOULD return and accept caching headers.



[develhub]: http://developers.erasmuswithoutpaper.eu/
[discovery-api]: https://github.com/erasmus-without-paper/ewp-specs-api-discovery
[error-handling]: https://github.com/erasmus-without-paper/ewp-specs-architecture#error-handling
[omobilities-spec]: https://github.com/erasmus-without-paper/ewp-specs-api-omobilities
[sec-v2]: https://github.com/erasmus-without-paper/ewp-specs-sec-intro/tree/stable-v2
[statuses]: https://github.com/erasmus-without-paper/ewp-specs-management#statuses
