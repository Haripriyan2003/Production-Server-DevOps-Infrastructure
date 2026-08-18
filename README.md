# Production Server & DevOps Infrastructure

A production-grade dedicated server infrastructure designed, configured, secured, monitored, and maintained for hosting multiple applications, APIs, databases, monitoring services, and AI workloads.

> **Security Notice:**
> This repository is intended only to document my DevOps and Linux administration experience.
> Sensitive company infrastructure information such as IP addresses, credentials, internal domains, firewall configurations, application secrets, database credentials, private monitoring endpoints, and production configuration files are intentionally excluded.

---

## Project Overview

This project represents my hands-on experience in building and managing a dedicated production server environment for real-world applications.

The infrastructure was designed to support:

* Production websites
* Backend APIs
* Node.js applications
* Databases
* WebSocket services
* Application monitoring
* Infrastructure monitoring
* Centralized logging
* AI-powered applications
* Local AI/LLM workloads

The server environment was configured with a focus on **performance, monitoring, reliability, security, and production maintainability**.

---

## Server Environment

The production environment is hosted on dedicated hardware with approximately:

* **20 vCPUs**
* **96 GB RAM**
* **2 TB Storage**
* Enterprise Linux-based operating environment

The actual server identity, network information, and production access details are intentionally not published.

---

## Technologies Used

### Server Administration

* Linux
* AlmaLinux
* cPanel / WHM
* SSH
* systemd
* Bash
* Cron
* Linux permissions and ownership management
* Service management
* Disk and resource management

### Web Infrastructure

* Nginx
* Apache
* Reverse Proxy
* SSL/TLS
* DNS configuration
* Subdomain management
* Wildcard SSL
* Application routing

### Application Runtime

* Node.js
* PM2
* PHP
* Python
* WebSocket / Socket.IO services

### Databases & Storage

* MariaDB / MySQL
* Redis
* Object storage solutions

### Monitoring

* Prometheus
* Grafana
* Custom application metrics
* Server resource monitoring
* Process monitoring

### Logging & Observability

* Elasticsearch
* Logstash
* Kibana
* ELK Stack
* Centralized application logging
* Log analysis
* Production troubleshooting

### Artificial Intelligence

The server also supports AI-powered workloads and local AI model experimentation.

Technologies include:

* Qwen-family LLM workloads
* AI API integrations
* Local model execution
* AI-powered backend services

---

# Infrastructure Architecture

At a high level, the production environment follows an architecture similar to:

```text
                     Internet
                         |
                         |
                  DNS / SSL Layer
                         |
                         v
                      Nginx
                         |
              +----------+----------+
              |                     |
              v                     v
           Apache               Node.js
          Websites                APIs
                                   |
                                   |
                     +-------------+-------------+
                     |             |             |
                     v             v             v
                  MariaDB        Redis        AI Services


                Monitoring & Observability
                         |
             +-----------+-----------+
             |                       |
             v                       v
        Prometheus                  ELK
             |                       |
             v                       v
          Grafana                  Kibana
```

This diagram is intentionally simplified and does not represent the exact internal production network architecture.

---

# Prometheus & Grafana Monitoring

Prometheus and Grafana were implemented to improve visibility into the production environment.

Monitoring includes areas such as:

* CPU utilization
* Memory utilization
* Server availability
* Application process status
* Application uptime
* Process restarts
* Application resource consumption
* Service health
* Backend service monitoring

Grafana dashboards provide centralized visualization of infrastructure and application health.

Alerts can be configured to identify service failures or abnormal behavior before they significantly affect production applications.

---

# ELK Stack

A centralized logging platform was implemented using:

**Elasticsearch + Logstash + Kibana**

The ELK Stack helps collect, analyze, search, and visualize application and server logs.

### Use Cases

* Application troubleshooting
* Error analysis
* Centralized log management
* Production incident investigation
* API error tracking
* Service monitoring
* Log searching
* Operational analysis

Centralized logging significantly improves debugging compared with manually checking individual application log files.

---

# Application Process Management

Node.js applications are managed using **PM2**.

PM2 is used for:

* Running Node.js production applications
* Process monitoring
* Restarting crashed applications
* Managing multiple Node.js services
* Application log handling
* Startup configuration
* Process status monitoring

Custom monitoring integrations are also used to expose application process metrics to Prometheus and Grafana.

---

# Reverse Proxy Architecture

Nginx is used as an important part of the production web infrastructure.

It handles tasks such as:

* Reverse proxying
* HTTPS traffic handling
* Application routing
* Domain and subdomain routing
* WebSocket proxying
* Forwarding requests to backend applications

Multiple backend applications can therefore operate independently while being accessed securely through standard HTTPS endpoints.

---

# SSL & Domain Management

The environment includes production SSL/TLS configuration for hosted websites and applications.

Experience gained includes:

* SSL certificate management
* HTTPS configuration
* Wildcard SSL certificates
* Subdomain SSL
* DNS configuration
* Reverse proxy SSL
* Application HTTPS troubleshooting

No private certificates, keys, DNS records, or production infrastructure information are stored in this repository.

---

# WebSocket Infrastructure

The production environment also supports real-time applications using technologies such as:

* WebSocket
* Socket.IO
* Node.js
* Nginx reverse proxy

This includes configuring Nginx correctly for WebSocket upgrade connections and forwarding traffic securely to backend services.

---

# AI Workloads

The infrastructure is also used for experimenting with and running AI-powered services.

This includes working with:

* Large Language Models
* Qwen-family models
* AI APIs
* Backend AI integrations
* Local AI model workloads

AI workloads are integrated alongside traditional web applications while infrastructure resources are monitored through the observability stack.

---

# Security Practices

Production infrastructure requires significantly more care than development environments.

Some of the practices followed include:

* Restricting unnecessary service exposure
* Managing Linux file permissions
* Using secure SSH access
* Protecting production credentials
* SSL/TLS encryption
* Service isolation
* Regular log monitoring
* Infrastructure monitoring
* Controlled application ports
* Environment-based application secrets
* Limiting publicly exposed services

Sensitive security configurations are intentionally not included in this repository.

---

# Troubleshooting Experience

Building and operating this environment provided hands-on experience troubleshooting issues including:

* Nginx configuration problems
* Reverse proxy issues
* WebSocket connectivity
* SSL certificate problems
* DNS configuration
* Linux service failures
* Node.js application failures
* PM2 process issues
* Port conflicts
* Database connectivity
* File permission problems
* Resource utilization
* Monitoring configuration
* Log analysis
* Production application errors

---

# Key Responsibilities

My responsibilities for this infrastructure include:

* Linux server administration
* Production server configuration
* cPanel/WHM administration
* Nginx configuration
* Application deployment
* Node.js process management
* SSL configuration
* DNS configuration
* Database administration
* Monitoring implementation
* Grafana dashboard creation
* Prometheus configuration
* ELK Stack implementation
* Log analysis
* Production troubleshooting
* Performance monitoring
* AI workload integration

---

# Skills Demonstrated

This project demonstrates hands-on experience with:

`Linux`

`AlmaLinux`

`DevOps`

`cPanel`

`WHM`

`Nginx`

`Apache`

`Node.js`

`PM2`

`MariaDB`

`MySQL`

`Redis`

`Prometheus`

`Grafana`

`Elasticsearch`

`Logstash`

`Kibana`

`ELK Stack`

`WebSocket`

`Socket.IO`

`SSL/TLS`

`DNS`

`Systemd`

`Linux Networking`

`Server Monitoring`

`Centralized Logging`

`Production Troubleshooting`

`AI / LLM Infrastructure`

---

# What I Learned

Building and maintaining this production infrastructure strengthened my understanding of how different components of a real production system work together.

Instead of working with individual technologies independently, this project provided practical experience connecting:

**Linux → Nginx → Applications → Databases → Monitoring → Logging → AI Services**

It also improved my ability to diagnose production problems systematically using metrics, application logs, Linux tools, and monitoring dashboards.

---

# Confidentiality

This project represents infrastructure developed and maintained within a company environment.

For security and confidentiality reasons, this repository does **not** contain:

* Production IP addresses
* Server hostnames
* SSH information
* Credentials
* Passwords
* API keys
* `.env` files
* Database credentials
* Customer information
* Internal application names
* Private source code
* Firewall rules
* Internal ports
* SSL private keys
* Production configuration files
* Internal architecture documentation

Only high-level technical information is shared to demonstrate my professional DevOps and Linux administration experience.

---

## Author

**Hari Priyan**

Web Developer | Linux Administrator | DevOps Enthusiast

GitHub: `Haripriyan2003`

---

## Project Status

**Production Infrastructure — Actively Managed**

This infrastructure continues to evolve as additional monitoring, automation, AI services, deployment practices, and production workloads are introduced.
