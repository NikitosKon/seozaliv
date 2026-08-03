# Infrastructure Bible

## Personal-edition deployment

Start with Docker Compose on one reliable host. Introduce Kubernetes only after workload and operational requirements justify it.

## Initial services

- Web application
- API/backend
- AI worker
- Background worker
- PostgreSQL
- Redis
- Object storage
- Qdrant
- Reverse proxy

## Environments

- Local development
- Staging or preview
- Production

## Observability

Use structured logs, traces, service metrics, task metrics, provider usage, AI cost, queue age, and workflow success rates.

## Secrets

Store provider keys, CMS credentials, and database credentials outside source control. Use encrypted environment management or a secret manager.

## Backups

Back up PostgreSQL and object storage. Test restoration periodically. Configuration and prompts remain versioned in Git.

## Scale triggers

Add specialized infrastructure only after measured pressure:

- ClickHouse for analytics volume
- OpenSearch for search complexity
- Kubernetes for deployment or worker scaling needs
- Kafka or NATS when Redis-backed task coordination is insufficient
