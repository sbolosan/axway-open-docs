---
title: Network traffic - AWS Gateway
linkTitle: Network traffic - AWS Gateway
draft: false
weight: 70
description: Traffic is always initiated by the Agent to AWS and AMPLIFY Central. No sessions are ever initiated back to the Agent.
---
{{< alert title="Note" color="primary" >}}The Axway API Gateway connectivity to AMPLIFY Central is currently available in an alpha review mode; current functionality and configuration may change before release. Therefore, this connectivity is available for trial use only and is not supported for production API management or connectivity.{{< /alert >}}

## Data destinations

The destination for:

* Agent Authentication data is `login.axway.com`

* AWS API Gateway data is  `apicentral.axway.com`

* API Event data is `ingestion-lumberjack.datasearch.axway.com`

## Communication ports

All outbound traffic is sent over SSL via TCP / UDP.

Open the following ports to benefit from all the Agent functionalities:

* Outbound:

    * `443/tcp`: port for communication to AMPLIFY Central and AWS

    * `453/tcp`: port for all API event data