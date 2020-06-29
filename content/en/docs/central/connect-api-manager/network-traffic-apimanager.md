---
title: Network traffic - API Manager
linkTitle: Network traffic - API Manager
draft: false
weight: 120
description: Traffic is always initiated by the Agent to API Manager, API Gateway, and AMPLIFY Central. No sessions are ever initiated back to the Agent.
---
{{< alert title="Note" color="primary" >}}The Axway API Gateway connectivity to AMPLIFY Central is currently available in an alpha review mode; current functionality and configuration may change before release. Therefore, this connectivity is available for trial use only and is not supported for production API management or connectivity.{{< /alert >}}

## Data destinations

The destination for:

* Agent Authentication data is `login.axway.com`

* API definition (Swagger or WSDL) and API documentation data is `apicentral.axway.com`

* API Event data, the transaction summary and headers, is `ingestion-lumberjack.datasearch.axway.com`

## Communication ports

All outbound traffic is sent over SSL via TCP / UDP.

Open the following ports to benefit from all the Agent functionalities:

* Outbound:

    * `443/tcp`: port for most communication to AMPLIFY Central

    * `453/tcp`: port for all API event data

Other Ports used but do not need to be opened:

* Internal:

    * `8075/tcp`: default port for communication to API Manager

    * `8090/tcp`: default port for communication to API Gateway

* Inbound (used for the agent status server):

    * `8989/tcp`: default port for serving the agent status

## Using proxies

A proxy can be set within the configuration file for all connections made by the agents.

### HTTP/HTTPS Proxy

Use a HTTP/HTTPS Proxy for communication to the AMPLIFY Platform.  This configuration is set for both the [Discovery](/docs/central/discovery-agent-variables/) and [Traceability Agents](/docs/central/traceability-agent-variables/).

### SOCKS5 Proxy

Use a SOCKS5 Proxy for communication to the AMPLIFY Platform when sending API Traffic Events.  This configuration is set only for [Traceability Agents](/docs/central/traceability-agent-variables/).