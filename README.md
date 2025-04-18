<div align="center">

# 🎟️ `KibanaCaseStudy` <!-- omit in toc -->

</div>

<div align="center">

| [Notion](https://atomic-warehouse.notion.site/KibanaCaseStudy-1d9eae73d15f8004b7a5c7ce6d52a9d1?pvs=4) |
| ----------------------------------------------------------------------------------------------------- |

</div>

🏴 A case study project for visualizing web traffic with ELK, ideal for learning log ingestion, parsing, and analytics.

## 📖 `Table Of Contents` <!-- omit in toc -->

- [🏷️ `Features`](#️-features)
- [🧑‍💻 `Mockaroo Field Setup`](#-mockaroo-field-setup)
- [🚥 `How To Run It`](#-how-to-run-it)
- [⛩️ `Achitecture Diagram`](#️-achitecture-diagram)
- [📊 `Dashboard Preview`](#-dashboard-preview)
  - [🔹 `Important Metrics Full Dashboard`](#-important-metrics-full-dashboard)
    - [📈 `Requests Over Time`](#-requests-over-time)
    - [📊 `Top Endpoints`](#-top-endpoints)
    - [🧾 `Response Codes`](#-response-codes)
    - [🧭 `Requests By Method`](#-requests-by-method)
    - [📦 `Bytes Transferred`](#-bytes-transferred)
    - [🕵️‍♂️ `Top User Agents`](#️️-top-user-agents)
    - [🌐 `Requests By IP`](#-requests-by-ip)
  - [📥 `Importing The Dashboard`](#-importing-the-dashboard)

---

# 🏷️ `Features`

- Ingests raw Nginx logs using Logstash
- Parses logs with GROK filters
- Visualizes data in Kibana dashboards
- Built with Elasticsearch, Logstash and Kibana 8.13.2

# 🧑‍💻 `Mockaroo Field Setup`

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

# 🚥 `How To Run It`

```bash
docker-compose up
```

Then visit http://localhost:5601

# ⛩️ `Achitecture Diagram`

<div align="center">

<img src=".github/diagram.png" width="50%" alt="Kibana Dashboard Preview" />

</div>

---

# 📊 `Dashboard Preview`

## 🔹 `Important Metrics Full Dashboard`

<img src=".github/dash-full.png" width="100%" alt="Kibana Dashboard Preview" />

#### 📈 `Requests Over Time`

![Requests Over Time](.github/requests-overtime.png)
_Shows number of requests per minute._

---

#### 📊 `Top Endpoints`

![Top Endpoints](.github/top-endpoints.png)
_Most accessed API routes._

---

#### 🧾 `Response Codes`

![Response Codes](.github/response-codes.png)
_Distribution of status codes._

---

#### 🧭 `Requests By Method`

![Requests By Method](.github/requests-by-method.png)
_HTTP methods used. (GET, POST, etc.)_

---

#### 📦 `Bytes Transferred`

![Bytes Transferred](.github/requests-overtime.png)
_Total traffic volume over time. GET, POST, etc._

---

#### 🕵️‍♂️ `Top User Agents`

![Top User Agents](.github/top-user-agents.png)
_Most active clients accessing the server._

---

#### 🌐 `Requests By IP`

![Requests By IP](.github/requests-by-ip.png)
_Top visitor IP addresses._

---

## 📥 `Importing The Dashboard`

1. Go to "Management → Stack Management → Saved Objects"
2. Click “Import”
3. Upload the .ndjson file
4. Click “Import”

---
