---
title: Working with Flask
---

{{< mermaid class="text-center" >}}
sequenceDiagram
box Client
    participant b as browser
end
participant f as webserver <br/>(flask)

Note over b: User clicks on a link
b->>+f: requests page
Note over f: determines which function<br/> to call based on routes
create participant h as function
f->>+h: runs handler with request
Note over h: does stuff, <br/>probably including <br/>query a database
create participant d as database
h->>+d: submits database query
Note over d: executes query
d->>-h: returns response
Note over h: prepares data for template
create participant j as jinja
h->>+j: calls jinja with <br/>template to render <br/>and data to use
Note over j: renders template
j->>-h: returns rendered template
h->>-f: returns completed response
f->>-b: sends response to client
Note over b: client renders response <br/>as appropriate
{{< /mermaid >}}