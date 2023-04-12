# EdgeQL 
EdgeQL is a fast GraphQL CDN on Cloudflare Edge, delivering optimized GraphQL responses with low latency. Easy to use and integrate, EdgeQL leverages Cloudflare's powerful caching and delivery network for improved performance and reliability.

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/0bl/edgeql)

### How it works
```mermaid
flowchart LR
    subgraph Client[Your GraphQL Client]
        query
        mutation
    end

    subgraph EdgeQL
        cache
    end

    subgraph Backend[Your GraphQL Backend]
        server
    end

    query <--> cache
    mutation <--> cache
    cache <--> server
```
