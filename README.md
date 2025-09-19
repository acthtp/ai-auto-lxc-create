```mermaid
flowchart TD
  A[User] --> B[AI]
  B --> C[MCP]
  C --> D[Proxmox]
  D --> E[LXC]
  C --> F[GitHub]
  E --> G[Running App]
  G --> A

