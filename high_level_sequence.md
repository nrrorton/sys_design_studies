## High-Level System Design Sequence

### 1. Client
Who is using the system?
- Mobile app
- Web app
- Other clients

### 2. API / Backend
Where does the request enter the system?
- API gateway / load balancer
- Authentication
- Request routing

### 3. Core Application / Services
What actually processes the request?
- Business logic
- Request orchestration
- Recommendation service
- Other domain-specific services

### 4. Persistent Data
What information does the system need to store?
- Users / preferences
- Businesses / locations
- Reviews
- Application data
- Relational and/or other databases

### 5. External Dependencies
What information or capabilities come from outside our system?
- Maps / routing
- Business hours
- Campus occupancy
- Other third-party APIs

### 6. AI Layer
Where does AI actually provide value?
- LLM
- Embeddings / vector search
- RAG
- Tool calling
- Agentic workflows, if actually necessary

### 7. Supporting Infrastructure
What helps the system operate reliably at scale?
- Caching
- Queues / asynchronous processing
- Load balancing
- Rate limiting
- Monitoring / logging
- Replication / failover