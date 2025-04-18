# KibanaCaseStudy
🏴 A simple ELK stack project to visualize access logs using Docker Compose.

## Features
- Ingests raw Nginx logs using Logstash
- Parses logs with GROK filters
- Visualizes data in Kibana dashboards
- Built with Elasticsearch 7.17 and Kibana 7.17

## Mockaroo Fields Setup
| Field Name   | Type         | Custom Format / Format                                        |
|--------------|--------------|---------------------------------------------------------------|
| ip_address   | IP Address   |                                                               |
| dash1        | Custom List  | -                                                             |
| dash2        | Custom List  | -                                                             |
| timestamp    | Datetime     |                                                               |
| method       | Custom List  | GET, POST, PUT, DELETE                                        |
| endpoint     | Custom List  | /, /login, /products, /about, /contact, /admin                |
| protocol     | Custom List  | HTTP/1.0, HTTP/1.1, HTTP/2                                    |
| status_code  | Custom List  | 200, 301, 302, 404, 500, 403                                  |
| bytes        | Number       | Min: 20, Max: 5000                                            |
| referrer     | Custom List  | "-"                                                           |
| user_agent   | Custom List  | "Mozilla/5.0", "curl/7.64.1", "PostmanRuntime/7.26.8"         |

## How To Run It
```bash
docker-compose up
```

Then visit http://localhost:5601

## How To Import The Dashboard
1. Go to Stack Management → Saved Objects
2. Click “Import”
3. Upload the .ndjson file
4. Click “Import”

---
