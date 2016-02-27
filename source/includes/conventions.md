# Conventions

To make things easier, we have established several conventions that can be
used when interacting with the Statusy API:

1. All objects will be singular. For example, accessing team settings is done in
`/team` endpoints.
2. All endpoints are predicated with `/api` followed by the API version (version
1 if you are reading this documentation) so the full predicate is `/api/v1`.
3. All endpoints use standard request types (POST is create, PUT is for updates, etc.)
