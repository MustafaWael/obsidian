# Complete Networking Concepts List

## 1. Internet Fundamentals
- IP Address (IPv4, IPv6, Public, Private, Localhost)
- Port numbers (0-65535, well-known ports 80/443/3000/8080/22)
- Protocol (rules for communication)
- Packet (data chunk with header and payload)
- Client-Server Model (request-response cycle)
- Router (network traffic director)
- MAC Address (hardware identifier)
- Subnet (network segment)
- NAT (Network Address Translation)
- Firewall (traffic filter)

## 2. HTTP (HyperText Transfer Protocol)
- HTTP Methods: GET, POST, PUT, PATCH, DELETE, OPTIONS, HEAD
- HTTP Status Codes: 1xx (Informational), 2xx (Success), 3xx (Redirection), 4xx (Client Error), 5xx (Server Error)
- HTTP Headers: Request headers, Response headers
- HTTP Versions: HTTP/1.0, HTTP/1.1, HTTP/2, HTTP/3
- Request Line (method, URL, version)
- Response Line (version, status code, status text)
- Message Body (payload)
- Query Parameters (URL encoding)
- Path Parameters (REST API)
- Content-Type (MIME types: application/json, text/html, image/png)
- Accept header (content negotiation)
- User-Agent header (client identification)
- Authorization header (authentication schemes: Bearer, Basic, Digest)
- Cookie header (session management)
- CORS headers (Access-Control-Allow-Origin, Access-Control-Allow-Methods, Access-Control-Allow-Headers)
- Cache-Control header (caching directives)
- ETag header (resource versioning)
- Last-Modified header (timestamp)
- Location header (redirects)
- Referer header (source page)

## 3. HTTPS and Security
- TLS (Transport Layer Security)
- SSL (Secure Sockets Layer, deprecated)
- TLS Handshake (client hello, server hello, key exchange)
- TLS Versions: 1.0, 1.1, 1.2, 1.3
- 0-RTT (Zero Round Trip Time)
- 1-RTT (One Round Trip Time)
- Certificate (X.509 format)
- Certificate Authority (CA)
- Domain Validation (DV)
- Organization Validation (OV)
- Extended Validation (EV)
- Self-signed certificate
- Certificate Chain (root, intermediate, leaf)
- Public Key Infrastructure (PKI)
- Public Key (encryption)
- Private Key (decryption)
- Symmetric Encryption (session keys)
- Asymmetric Encryption (public/private key pair)
- Cipher Suite (encryption algorithms)
- Perfect Forward Secrecy (PFS)
- HSTS (HTTP Strict Transport Security)
- HPKP (HTTP Public Key Pinning, deprecated)

## 4. DNS (Domain Name System)
- Domain Name (human-readable address)
- FQDN (Fully Qualified Domain Name)
- TLD (Top Level Domain: .com, .org, .net)
- ccTLD (Country Code TLD: .uk, .de, .jp)
- Subdomain (www, api, blog)
- DNS Resolution (name to IP translation)
- DNS Resolver (recursive resolver)
- Root Name Server
- TLD Name Server
- Authoritative Name Server
- DNS Record Types: A, AAAA, CNAME, MX, TXT, NS, SOA, PTR, SRV, CAA
- DNS Caching (TTL - Time To Live)
- DNS Propagation
- Reverse DNS (PTR lookup)
- DNS Zone (administrative space)
- DNSSEC (DNS Security Extensions)
- DoH (DNS over HTTPS)
- DoT (DNS over TLS)
- EDNS Client Subnet (ECS)
- Anycast DNS (distributed DNS servers)
- Dynamic DNS (DDNS)

## 5. TCP (Transmission Control Protocol)
- Connection-oriented protocol
- Three-way Handshake (SYN, SYN-ACK, ACK)
- Four-way Termination (FIN, ACK)
- TCP Segment (packet structure)
- Sequence Number (ordering)
- Acknowledgment Number (receipt confirmation)
- Window Size (flow control)
- Congestion Window (congestion control)
- Slow Start (initial transmission rate)
- Congestion Avoidance (steady state)
- Fast Retransmit (quick recovery)
- Fast Recovery (after loss)
- Head-of-Line Blocking
- TCP_NODELAY (Nagle's algorithm disable)
- Keep-Alive (connection persistence)
- Maximum Segment Size (MSS)
- Time Wait state
- Close Wait state

## 6. UDP (User Datagram Protocol)
- Connectionless protocol
- Unreliable delivery
- No ordering guarantees
- No congestion control
- Low latency
- Datagram (UDP packet)
- Checksum (error detection)
- Used by: DNS, QUIC, WebRTC, gaming, streaming

## 7. QUIC and HTTP/3
- QUIC protocol (Quick UDP Internet Connections)
- HTTP/3 (HTTP over QUIC)
- Connection ID (persistent identifier)
- Connection Migration (IP change survival)
- Stream multiplexing (independent streams)
- 0-RTT resumption (instant reconnect)
- Forward Error Correction (FEC)
- Integrated TLS 1.3
- UDP-based transport
- Head-of-Line Blocking elimination
- Congestion control: BBR, CUBIC

## 8. WebSockets
- WebSocket protocol (ws://, wss://)
- WebSocket Handshake (HTTP Upgrade)
- Persistent connection
- Full-duplex communication
- Frame-based messaging
- Text frames
- Binary frames
- Ping/Pong frames (keepalive)
- Close frames
- WebSocket API (browser interface)
- Socket.io (WebSocket library)
- Reconnection strategies
- Message broadcasting
- Room/channel concept

## 9. WebTransport
- WebTransport API
- HTTP/3 based
- Datagram API (unreliable)
- Stream API (reliable)
- Bidirectional streams
- Unidirectional streams
- Out-of-order delivery option
- Congestion control integration
- Alternative to WebSocket

## 10. Server-Sent Events (SSE)
- EventSource API
- Unidirectional server-to-client
- Text-based protocol
- Automatic reconnection
- Event ID (resumption)
- Last-Event-ID header
- text/event-stream MIME type
- Multi-line data support

## 11. Caching
- Browser Cache
- HTTP Caching
- Cache-Control directives: max-age, no-cache, no-store, public, private, must-revalidate, immutable, s-maxage
- Expires header
- ETag (entity tag)
- Last-Modified
- If-None-Match (conditional request)
- If-Modified-Since (conditional request)
- Vary header
- Cache busting (versioned filenames)
- Service Worker Cache (Cache API)
- LocalStorage (persistent storage)
- SessionStorage (tab-scoped storage)
- IndexedDB (structured storage)
- Memory Cache (RAM)
- Disk Cache (hard drive)
- Push Cache (HTTP/2 server push)
- CDN Cache (edge servers)
- Application Cache (deprecated AppCache)

## 12. CDNs and Edge Computing
- CDN (Content Delivery Network)
- Origin Server (source)
- Edge Server (cache location)
- Point of Presence (PoP)
- Anycast routing
- GeoDNS (geographic DNS)
- Edge caching
- Cache invalidation
- Purge/Flush cache
- Stale-while-revalidate
- Edge computing (Cloudflare Workers, Lambda@Edge)
- DDoS protection (distributed denial of service)

## 13. Performance Optimization
- DNS Prefetch
- Preconnect
- Prefetch
- Preload
- Prerender
- Resource Hints
- Critical Rendering Path
- First Contentful Paint (FCP)
- Largest Contentful Paint (LCP)
- First Input Delay (FID)
- Cumulative Layout Shift (CLS)
- Time to First Byte (TTFB)
- Time to Interactive (TTI)
- Total Blocking Time (TBT)
- Speed Index
- Round Trip Time (RTT)
- Latency (ping time)
- Bandwidth (data capacity)
- Throughput (actual data rate)
- Jitter (latency variation)
- Packet Loss (missing data)
- Compression: gzip, brotli, deflate
- Minification (code reduction)
- Bundling (file combination)
- Code splitting (lazy loading)
- Tree shaking (dead code elimination)
- Image optimization (WebP, AVIF, responsive images)
- Lazy loading (intersection observer)
- Priority hints (fetchpriority)
- Resource loading: async, defer, module

## 14. Security Concepts
- XSS (Cross-Site Scripting)
- CSRF (Cross-Site Request Forgery)
- SQL Injection
- Clickjacking
- Man-in-the-Middle (MitM)
- Replay Attack
- Session Hijacking
- Cookie Security: HttpOnly, Secure, SameSite, Domain, Path, Expires, Max-Age
- CSP (Content Security Policy)
- SRI (Subresource Integrity)
- X-Frame-Options (clickjacking protection)
- X-XSS-Protection
- X-Content-Type-Options (MIME sniffing)
- Referrer-Policy
- Permissions-Policy
- Feature-Policy (deprecated)
- Mixed Content (HTTP on HTTPS page)
- Secure Context (HTTPS, localhost, file)
- OAuth 2.0 (authorization framework)
- JWT (JSON Web Token)
- SSO (Single Sign-On)
- 2FA/MFA (Two-Factor/Multi-Factor Authentication)
- Rate Limiting (throttling)
- DDoS Mitigation

## 15. API Design and Patterns
- REST (Representational State Transfer)
- RESTful principles: statelessness, cacheability, layered system, uniform interface
- HTTP verbs usage
- Resource naming (nouns not verbs)
- Status code appropriateness
- HATEOAS (Hypermedia as Engine of Application State)
- GraphQL (query language)
- gRPC (RPC framework over HTTP/2)
- tRPC (TypeScript RPC)
- Webhooks (event callbacks)
- Long Polling (simulated real-time)
- Server-Sent Events (SSE)
- API Versioning (URL, header, content negotiation)
- Pagination: offset, cursor, keyset
- Filtering, Sorting, Field selection
- Rate limiting headers: X-RateLimit-Limit, X-RateLimit-Remaining, X-RateLimit-Reset
- API Authentication: API Keys, OAuth, JWT, Basic Auth, Bearer Token
- OpenAPI (Swagger specification)
- Postman/Insomnia (API testing)
- CORS Preflight (OPTIONS request)
- Simple request vs Preflighted request

## 16. Network Architecture
- Monolith (single application)
- Microservices (distributed services)
- Service Mesh (Istio, Linkerd)
- Load Balancer (traffic distribution)
- Reverse Proxy (Nginx, Apache)
- API Gateway (Kong, AWS API Gateway)
- Edge Gateway
- Service Discovery (Consul, Eureka)
- Circuit Breaker (failure protection)
- Retry Logic (exponential backoff)
- Timeout handling
- Health Checks (liveness, readiness)
- Blue-Green Deployment
- Canary Release
- A/B Testing
- Feature Flags

## 17. DevOps and Deployment
- CI/CD (Continuous Integration/Deployment)
- Docker (containerization)
- Kubernetes (container orchestration)
- Serverless (Lambda, Cloud Functions)
- Static Site Hosting (Netlify, Vercel)
- PaaS (Platform as a Service: Heroku)
- IaaS (Infrastructure as a Service: AWS EC2)
- FaaS (Function as a Service)
- Edge Deployment (Cloudflare Pages)
- SSL/TLS Certificate Management (Let's Encrypt, Certbot)
- Reverse Proxy Configuration
- Environment Variables
- Secrets Management (HashiCorp Vault, AWS Secrets Manager)

## 18. Monitoring and Debugging
- Browser DevTools: Network tab, Performance tab, Application tab, Console, Sources
- Lighthouse (auditing tool)
- WebPageTest (performance testing)
- GTmetrix (speed analysis)
- Pingdom (uptime monitoring)
- Sentry (error tracking)
- LogRocket (session replay)
- Datadog (APM)
- New Relic (performance monitoring)
- Wireshark (packet analysis)
- tcpdump (command line packet capture)
- curl (HTTP client)
- Postman (API client)
- Charles Proxy (HTTP proxy)
- Fiddler (debugging proxy)
- ngrok (tunneling)
- browser-sync (development server)

## 19. Protocols and Standards
- TCP/IP Stack (Internet protocol suite)
- OSI Model (7 layers: Physical, Data Link, Network, Transport, Session, Presentation, Application)
- URI (Uniform Resource Identifier)
- URL (Uniform Resource Locator)
- URN (Uniform Resource Name)
- IANA (Internet Assigned Numbers Authority)
- W3C (World Wide Web Consortium)
- IETF (Internet Engineering Task Force)
- RFC (Request for Comments)
- WHATWG (Web Hypertext Application Technology Working Group)
- ECMAScript (JavaScript standard)
- Fetch API Standard
- XMLHttpRequest (legacy AJAX)
- WebRTC (Real-Time Communication)
- WebAssembly (Wasm)
- Progressive Web App (PWA) standards

## 20. Emerging and Advanced Topics
- HTTP/3 adoption
- QUIC protocol details
- WebAssembly System Interface (WASI)
- Edge Functions (Vercel Edge, Cloudflare Workers)
- Distributed Systems (CAP theorem)
- Event-Driven Architecture
- Message Queues (RabbitMQ, Kafka)
- WebSub (PubSubHubbub)
- ActivityPub (decentralized social networking)
- IPFS (InterPlanetary File System)
- Blockchain/Web3 concepts
- Web5 (decentralized web identity)
- Server Components (React Server Components)
- Islands Architecture (Astro)
- Edge Rendering
- Streaming SSR (Server-Side Rendering)
- Partial Hydration
- Resumability (Qwik framework)