#  Visualize Telemetry with OpenTelemetry and .NET Aspire

## Overview

This repository allows to visualize traces, logs, and metrics all in one in the new .NET Aspire dashboard tool.

## Prerequisites

- [Net 8](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) installled.
- [Docker Desktop](https://docs.docker.com/desktop/install/windows-install/) installed.

## Setup

1. Clone o download this repository:

   ```bash
   git clone https://github.com/camiloJaramillo5/aspire-opentelemetry/
2. Download the docker image
   ```bash
   docker run --rm -it -p 18888:18888 -p 4317:18889 -d --name aspire-dashboard -e DOTNET_DASHBOARD_UNSECURED_ALLOW_ANONYMOUS='true' mcr.microsoft.com/dotnet/nightly/aspire-dashboard:8.0.0-preview.6
3. Build and run the web API project.
5. Hit the endpoint repeatedly and wait some time for OTEL to collect and export the data.
6. Verify in the URL http://localhost:18888/ the results. You should see similar results as these:
   ![image](https://github.com/camiloJaramillo5/aspire-opentelemetry/assets/80411997/76094bef-372d-436f-bf3f-987055963406)
   ![image](https://github.com/camiloJaramillo5/aspire-opentelemetry/assets/80411997/f2fb05f3-3782-4920-a897-056b2335dd46)
   ![image](https://github.com/camiloJaramillo5/aspire-opentelemetry/assets/80411997/75d6d614-38e9-4ed3-a9cf-dfea9bb26861)



