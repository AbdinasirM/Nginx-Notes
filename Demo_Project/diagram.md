### Diagram: Docker Setup
```
[Docker Containers]
   ┌──────────────┬──────────────┬──────────────┐
   │   app1       │   app2       │   app3       │
   │   Port 3001  │   Port 3002  │   Port 3003  │
   └──────────────┴──────────────┴──────────────┘
```

### Diagram: NGINX Setup
```
[Browser/Client]
       |
       V
   [NGINX Proxy Server] -- HTTPS --> [Docker Apps]
                          ┌─────────────────────────┐
                          │    nodejs_cluster       │
                          │ ┌────────┬────────┬────┐ │
                          │ │ app1   │ app2   │ app3 │ │
                          │ │:3001   │:3002   │:3003 │ │
                          │ └────────┴────────┴────┘ │
                          └─────────────────────────┘
```
