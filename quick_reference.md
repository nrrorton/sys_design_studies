# System Design Quick Reference

## Requirements
- What must the system do?
- What are the core user flows?
- Don't confuse functionality with implementation.

## NFRs
- Scalability
- Availability
- Performance / latency
- Reliability
- Security / privacy
- Cost

## Capacity
DAU → requests/day → average QPS → peak QPS

Ask:
- What does one request fan out into?
- Which dependency becomes the bottleneck?
- What are the rate limits?

## High-Level Architecture
Client
→ API / Backend
→ Core Services
→ Data + External Services
→ AI
→ Response

Supporting:
- Cache
- Queue
- Load balancing
- Rate limiting
- Monitoring
- Replication / failover

## AI
LLM       → language understanding / synthesis
Embedding → semantic representation
Vector DB → vector storage / similarity search
RAG       → retrieve context → give it to LLM
Tool      → external capability / authoritative data
Agent     → dynamic multi-step reasoning + tool use

## AI Rule
Don't make the LLM determine facts that a reliable system
can provide directly.

Examples:
- Distance → routing service
- Hours → business API
- User preferences → database
- Review meaning → semantic retrieval
- Explanation → LLM

## Reliability
Ask:
- What if it's slow?
- What if it fails?
- What if it's unavailable?
- What if it's rate-limited?
- Can we cache it?
- Can we fall back?
- Can we degrade gracefully?

## Deep Dive
Pick 1–2 genuinely difficult components.
Explain:
1. Why it's difficult
2. How it works
3. Bottlenecks
4. Failure modes
5. Scaling strategy