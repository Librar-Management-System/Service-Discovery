# 🔍 Library Management System — Service Discovery

## 🚀 Overview
- Provides dynamic service registration and lookup for LMS microservices  
- Allows services to communicate without hard-coded URLs  
- Ensures scalability, load balancing, and fault tolerance  
- Forms the backbone of internal communication between all services  

---

## 🔑 Key Responsibilities
- **Service Registration** – Each service registers itself on startup  
- **Service Lookup** – Other services request the latest healthy instance  
- **Health Checks** – Removes unhealthy or offline service instances  
- **Dynamic Updates** – Automatically handles scaling (add/remove instances)  
- **Load Balancing Support** – Works with gateway or client-side load balancers  

---

## 🏗 Architecture
- Microservices  
  → **Register** with Service Discovery  
- API Gateway  
  → **Fetches** service addresses via Service Discovery  
- Supports:
  - Consul  
  - Eureka  
  - etcd  
  

---

## ⚙️ Configuration
Set discovery settings using environment variables.

Important environment variables:
- `DISCOVERY_BACKEND` – consul / eureka / etcd / kubernetes  
- `DISCOVERY_URL` – service registry endpoint  
- `HEALTH_INTERVAL` – health check frequency  
- `SERVICE_TTL` – time-to-live before an instance expires  
- `ACL_TOKEN` – secure write access token  

---
