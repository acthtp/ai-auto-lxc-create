flowchart TD
    U[👤 User<br/>Command: "Create LXC with Python"] --> A[🤖 AI (Codex)<br/>Generates instructions]
    A --> M[🖧 MCP Server<br/>(exec / http / git / fs)]
    M -->|exec| S[📜 Scripts on Proxmox Host<br/>create_lxc.sh<br/>bootstrap_base.sh<br/>deploy_<lang>.sh]
    M -->|http (API)| P[🖥️ Proxmox Host<br/>pct / qm / API / Pools & ACLs]
    M -->|git/github| G[🐙 GitHub<br/>Repo + Actions/Runner]
    S --> P
    P --> L[📦 LXC Container<br/>Base OS + Runtime/Docker]
    G --> L
    L --> R[🌐 Running App<br/>http://IP:PORT]
    R --> U

