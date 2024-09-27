---
title: "API Documentation"
date: 2024-09-17T12:00:00Z
draft: false
slug: "apidocs"
---


Welcome to the API documentation for services hosted at `api.cameronmichelis.com`. Below are the available API endpoints, their functionality, and the authentication requirements.  If you’re interested in accessing a protected APIs, feel free to [contact me](/contact/) to request an API key.

---

## Public Endpoints (No Authentication Required)

### 1. **GET /v1/echo**
https://api.cameronmichelis.com/v1/echo

**Description**: The Echo service risk scores the request details sent by the client, including the HTTP method, headers, query parameters, and body (if present). This is useful for testing and debugging API requests.

**Endpoint**:  
`GET /v1/echo`

**Request Example**:
`curl -X GET "https://api.cameronmichelis.com/v1/echo?param=value"`


### 2. **GET /v1/status**
https://api.cameronmichelis.com/v1/status

**Description:** Returns the current status of the API services, including uptime and the operational state of the security, geolocation, and MISP services.

**Endpoint:**
`GET /v1/status`

**Request Example**:
`curl -X GET "https://api.cameronmichelis.com/v1/status"`

---
## Protected Endpoints (Authentication Required)

## 3. GET /v1/geolocation
**Description:** Provides geolocation data based on an IP address. 

## 4. GET /v1/misp/threat-intelligence
**Description:** Fetches threat intelligence data from the MISP platform, including information on IOCs (Indicators of Compromise).

## 5. POST /v1/misp/iocs
**Description:** Submits a new Indicator of Compromise (IOC) to the MISP platform. This service requires authentication via an API key.
## 6. GET /v1/misp/events
**Description:** Allows searching for events in the MISP platform using query parameters. This service requires authentication via an API key.

## 7. POST /v1/misp/sync
**Description:** Initiates synchronization of threat intelligence data between MISP instances. This service requires authentication via an API key.


