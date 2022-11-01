# Sample Go API Gateway Using httputil.ReverseProxy

```
.
├── config
│   └── default.yml -- Gateway Configuration
├── go.mod 
├── go.sum
├── main.go
└── README.md <-- You are here.
```

Sample Gateway Configuration.
```
gateway:
  listenAddr: localhost:8080                # Server listens on this.
  routes:
    - name: Service A
      context: /service-a                   # The context root to match.
      target: http://localhost:8082         # The target url to forward the request to.
    - name: Service B
      context: /service-b                   # So on and so forth.
      target: http://localhost:8081
```