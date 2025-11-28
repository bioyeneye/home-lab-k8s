## LoadBalancer Access (Internal Network Only)

Rancher is configured with MetalLB LoadBalancer for internal network access only.

**IP Address:** 172.16.0.104

### Access Methods:

1. **Direct IP Access:**
```
   https://172.16.0.104
```

2. **Using sslip.io (avoids cert hostname mismatch):**
```
   https://172.16.0.104.sslip.io
```

3. **Using /etc/hosts:**
```bash
   # Add to /etc/hosts
   172.16.0.104 rancher.local
   
   # Access
   https://rancher.local
```

### Certificate Warning:

- Rancher uses self-signed certificates by default
- You'll see a certificate warning in your browser - this is expected
- Click "Advanced" → "Proceed" (or equivalent in your browser)

### Network Requirements:

- Must be on the same network as your K8s cluster
- IP: 172.16.0.104
- Ports: 80 (HTTP) and 443 (HTTPS)
- No external/internet access required