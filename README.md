# 🛡️ Azure Cyber Honeypot Lab: Real-Time Attack Mapping with Microsoft Sentinel

## Project Goal: 
To create a functional Security Operations Center (SOC) lab environment using cloud services to observe and map real-world attack traffic against a public-facing Honeypot.
You’ll learn how to design, deploy, and operate a home-lab environment that simulates real-world scenarios. The goal is to give security enthusiasts, students, and IT professionals a safe sandbox to practise detecting and preventing attacks, without needing expensive hardware or overly complex setups.

## Technology Stack:

Cloud: Azure (VMs, Network Security Group, Public IP)

SIEM: Microsoft Sentinel

Log Ingestion: Azure Log Analytics Workspace (LAW) and Azure Monitoring Agent

Query Language: Kusto Query Language (KQL)

Core Components:

Honeypot: Windows 10/Server VM with open RDP/SSH ports.

Log Repository: Azure Log Analytics Workspace.

Visualization: Sentinel Workbook (Attack Map) enriched with Geo-IP data.

## 🏗️ Architecture and Data Flow
The architecture follows a standard logging pipeline, from the source (Honeypot) to the analysis platform (Sentinel).

Honeypot VM: Exposed to the public internet via an open Network Security Group (NSG) and disabled internal firewall.

Log Ingestion: The Azure Monitoring Agent (AMA) forwards Windows Security Events (specifically Event ID 4625 for failed logons) from the VM.

Log Repository: Logs are stored in the Azure Log Analytics Workspace (LAW).

Analysis: Microsoft Sentinel connects to the LAW. A Geo-IP Watchlist is imported for data enrichment.

Visualization: A custom Sentinel Workbook uses KQL to join the failed logon events with the Geo-IP data, plotting the attacker's location on the Attack Map.

View the full diagram in documentation/Architecture_Diagram.png.

## 🎯 Key Project Highlights & Results
Real-World Data: Observed thousands of failed login attempts from botnets and malicious actors worldwide within hours of deployment.

Data Enrichment: Successfully imported a custom Geo-IP Watchlist and used KQL to perform a lookup/join operation, adding geographical coordinates (Latitude/Longitude) to raw security logs.

Custom Visualization: Created a dynamic Sentinel Workbook to transform raw text logs and IP addresses into an easy-to-interpret global Attack Map.

Cost Management: Established clear cleanup procedures and scripts to ensure the environment is de-provisioned promptly.
