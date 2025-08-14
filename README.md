# Task 7 – Monitor System Resources Using Netdata 

## Objective
Install and run **Netdata** to visualize system and Docker container performance on an EC2 Ubuntu server. Capture key dashboard screenshots and document the steps.

## Tools
- **EC2 Ubuntu** server
- **Docker** 
- Netdata Docker image: `netdata/netdata`

## Architecture (High Level)
Laptop Browser ⇄ SSH Tunnel (recommended) ⇄ EC2 Ubuntu (Docker) ⇄ Netdata Agent

---

## Prerequisites
- Docker running on EC2: `docker ps`
- SSH access to the instance
- Port strategy:
  - **Recommended:** SSH tunnel (no public port)
  - **Alternative:** Open SG TCP 19999 from **My IP** only

---

## Quick Start (One-liner)
```bash
docker run -d --name=netdata -p 19999:19999 netdata/netdata

