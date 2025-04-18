# KibanaCaseStudy

🏴 A simple ELK stack project to visualize access logs using Docker Compose.

## Features

- Ingests raw Nginx logs using Logstash
- Parses logs with GROK filters
- Visualizes data in Kibana dashboards
- Built with Elasticsearch 7.17 and Kibana 7.17

## Mockaroo Field Setup

| Field Name  | Type        | Custom Format / Format                                |
| ----------- | ----------- | ----------------------------------------------------- |
| ip_address  | IP Address  |                                                       |
| dash1       | Custom List | -                                                     |
| dash2       | Custom List | -                                                     |
| timestamp   | Datetime    |                                                       |
| method      | Custom List | GET, POST, PUT, DELETE                                |
| endpoint    | Custom List | /, /login, /products, /about, /contact, /admin        |
| protocol    | Custom List | HTTP/1.0, HTTP/1.1, HTTP/2                            |
| status_code | Custom List | 200, 301, 302, 404, 500, 403                          |
| bytes       | Number      | Min: 20, Max: 5000                                    |
| referrer    | Custom List | "-"                                                   |
| user_agent  | Custom List | "Mozilla/5.0", "curl/7.64.1", "PostmanRuntime/7.26.8" |

## How To Run It

```bash
docker-compose up
```

Then visit http://localhost:5601

# Architecture Diagram

<div align="center">

<img src=".github/diagram.png" width="50%" alt="Kibana Dashboard Preview" />

</div>

---

# 📊 Dashboard Preview

## 🔹 Important Metrics

<img src=".github/dash-full.png" width="100%" alt="Kibana Dashboard Preview" />

### Individualized Visualizations

#### 📈 Requests Over Time

![Requests Over Time](.github/requests-over-time.png)
_Shows number of requests per minute._

---

#### 📊 Top Endpoints

![Top Endpoints](.github/top-endpoints.png)
_Most accessed API routes._

---

#### 🧾 Response Codes

![Response Codes](.github/response-codes.png)
_Distribution of status codes._

---

#### 🧭 Requests by Method

![Response Codes](.github/requests-by-method.png)
_HTTP methods used (GET, POST, etc.)_

---

#### 📦 Bytes Transferred

![Response Codes](.github/requests-overtime.png)
_Total traffic volume over time. GET, POST, etc._

---

#### 🕵️‍♂️ Top User Agents

![Response Codes](.github/top-user-agents.png)
_Most active clients accessing the server._

---

#### 🌐 Requests by IP

![Response Codes](.github/requests-by-ip.png)
_Top visitor IP addresses._

---

## Importing The Dashboard

1. Go to "Management → Stack Management → Saved Objects"
2. Click “Import”
3. Upload the .ndjson file
4. Click “Import”

---
