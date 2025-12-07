# 🛡️ Azure Cyber Honeypot Lab: Real-Time Attack Mapping with Microsoft Sentinel

Project Goal: To create a functional Security Operations Center (SOC) lab environment using cloud services to observe and map real-world attack traffic against a public-facing Honeypot.
You’ll learn how to design, deploy, and operate a home-lab environment that simulates real-world scenarios. The goal is to give security enthusiasts, students, and IT professionals a safe sandbox to practise detecting and preventing attacks, without needing expensive hardware or overly complex setups.

Technology Stack:

Cloud: Azure (VMs, Network Security Group, Public IP)

SIEM: Microsoft Sentinel

Log Ingestion: Azure Log Analytics Workspace (LAW) and Azure Monitoring Agent

Query Language: Kusto Query Language (KQL)

Core Components:

Honeypot: Windows 10/Server VM with open RDP/SSH ports.

Log Repository: Azure Log Analytics Workspace.

Visualization: Sentinel Workbook (Attack Map) enriched with Geo-IP data.
