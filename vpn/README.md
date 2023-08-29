# Docker Compose for VPN services
Copy this file to your desired directory, then run:

```docker compose up -d```

### This file will create three containers for home VPN services
* Cloudflare DDNS
Will keep your Cloudflare domain synced to your host IP
  * Add your API key for Cloudflare, will need permissions to read DNS zone
  * Zone is your domain name
  * Subdomain to match (if needed)
  
* WG-Easy
  
Simple Wireguard management with QR codes or configuration files
  * Access the web configuration at `your.host.ip:51821`

* Tailscale
  
For Zero-trust VPN management over a Wireguard framework
  * you will need to exec into the container and configure tailscale after installation:
  
  ```docker exec -it tailscale sh```

  Then run:

  ```tailscale up```

  and follow the prompts
