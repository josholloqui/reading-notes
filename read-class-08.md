# http basics
* HTTP stands for Hypertext Transfer Protocol. It's a stateless, application-layer protocol for communicating between distributed systems, and is the foundation of the modern web
* HTTP allows for communication between a variety of hosts and clients, and supports a mixture of network configurations.
* This makes HTTP a stateless protocol. The communication usually takes place over TCP/IP, but any reliable transport can be used. The default port for TCP/IP is 80, but other ports can also be used
* The client initiates an HTTP request message, which is serviced through a HTTP response message in return. We will look at this fundamental message-pair in the next section
* persistent connections, chunked transfer-coding and fine-grained caching headers
* web communications is the request message, which are sent via Uniform Resource Locators (URLs)
* GET: fetch an existing resource. The URL contains all the necessary information the server needs to locate and return the resource.
* POST: create a new resource. POST requests usually carry a payload that specifies the data for the new resource.
* PUT: update an existing resource. The payload may contain the updated data for the resource.
* DELETE: delete an existing resource.
* HEAD: this is similar to GET, but without the message body. It's used to retrieve the server headers for a particular resource, generally to check if the resource has changed, via timestamps.
* TRACE: used to retrieve the hops that a request takes to round trip from the server. Each intermediate proxy or gateway would inject its IP or DNS name into the Via header field. This can be used for diagnostic purposes.
* OPTIONS: used to retrieve the server capabilities. On the client-side, it can be used to modify the request based on what the server can support.
* With URLs and verbs, the client can initiate requests to the server. In return, the server responds with status codes and message payloads. The status code is important and tells the client how to interpret the server response

# How DNS Works
* The browser and the OS both searched their cache first to see if they knew the IP for dnsimple.com. But since they didn't, the OS is calling the resolver.
* The resolver server is usually your ISP (Internet Service Provider). All resolvers must know one thing: where to locate the root server.
* The root server knows where to locate the .COM TLD server. TLD stands for Top-Level Domain.
* Root servers sit at the top of the DNS hierarchy
* They are scattered around the globe and operated by 12 independent organisations
* They are named [letter].root-servers.net where [letter] ranges from A to M
* The coordination of most top-level domains (TLDs) belong to the Internet Corporation for Assigned Names and Numbers
* When a domain is purchased, the domain registrar reserves the name and communicates to the TLD registry the authoritative name servers
* You see, usually there is more than one name server attached to any domain

#### Video very informative bookmarked as well as the references 