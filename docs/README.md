---
icon: browser
---

# Interfaces used for interacting with web services

## REST API vs SCIM2 API

<table><thead><tr><th width="163"></th><th align="center">SCIM2 API</th><th align="center">REST API</th></tr></thead><tbody><tr><td>Definition</td><td align="center"><strong>System for Cross-domain Identity Management</strong><br>a <code>standard</code> for automating the exchange of user identity information between identity domains or IT systems</td><td align="center"><strong>Representational State Transfer</strong><br>an <code>architectural style</code> that uses standard <code>HTTP methods and status codes</code> for creating, reading, updating, and deleting resources.</td></tr><tr><td>Purpose</td><td align="center">User identity management</td><td align="center">General-purpose</td></tr><tr><td>Schema</td><td align="center">Standardized schema for identities</td><td align="center">Customizable based on use case</td></tr><tr><td>Interoperability</td><td align="center">High: industry standard</td><td align="center">Varies: depends on implementation</td></tr><tr><td>Use Cases</td><td align="center"><ul><li>User provisioning</li><li>Identity synch</li></ul></td><td align="center"><ul><li>CRUD operations on various resources</li><li>Building microservices and web applications</li></ul></td></tr><tr><td>Bulk Operations</td><td align="center">Supported</td><td align="center">Varies; required custom implementation</td></tr><tr><td>Extensibility</td><td align="center">Supports extensions</td><td align="center">Customizable by design</td></tr><tr><td>Key Features</td><td align="center"></td><td align="center"><strong>Statelessness</strong>: Each request from a client to server must contain all the information the server needs to fulfil that request<br><strong>Cacheable</strong>: Responses must define themselves as cacheable or not to prevent clients from reusing stale data<br><strong>Layered System</strong>: Client cannot ordinarily tell whether it is connected directly to the end server or to an intermediary along the way</td></tr><tr><td></td><td align="center"><pre><code>GET /scim/v2/Users
Content-Type: application/scim+json
Authorization: Bearer &#x3C;token>
</code></pre></td><td align="center"><pre><code>GET /api/users
Content-Type: application/json
Authorization: Bearer &#x3C;token>
</code></pre></td></tr></tbody></table>



