---
---

link:: https://braid.org

- Braid builds distributed features into today's web. We are an open group in the IETF.
- The **Braid Protocol** is an extension to HTTP that generalizes it from a state *transfer* to a state *synchronization* protocol.
  id:: 63d89d11-62ae-4607-9734-8420d691b241
- Braid adds these features to HTTP:
	- *Versioning* to HTTP resources
	- *Subscriptions* to GET requests
	- *Patches* to Range Requests
	- *Merge-Types* to specify OT or CRDT behavior
- Together, these features enable a web resource to synchronize automatically across multiple clients, servers and proxies, and support arbitrary simultaneous edits by multiple writers, under arbitrary network delays and partitions, while guaranteeing consistency using a [OT](https://en.wikipedia.org/wiki/Operational_transformation), [CRDT](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type), or other algorithm.
- #IETF draft https://datatracker.ietf.org/doc/html/draft-toomim-httpbis-braid-http
-