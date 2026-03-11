# GCP Incident Response Lab

## Overview
Simulated a full cloud security incident response on Google Cloud Platform 
as part of the Google Cloud Cybersecurity Certificate capstone.

## Scenario
A data breach at Cymbal Retail — compromised VM, exfiltrated credit card 
data via a public storage bucket, open SSH/RDP ports, no logging.

## What I Did
- Shut down and deleted the compromised VM
- Restored a clean instance from a pre-breach snapshot
- Revoked public bucket access & enforced IAM-only controls
- Created scoped firewall rule (IAP range 35.235.240.0/20, tag: cc)
- Deleted default-allow-ssh and default-allow-rdp rules
- Enabled logging across the environment
- Verified remediation via PCI DSS 3.2.1 report in Security Command Center

## Tools Used
- Google Cloud Security Command Center (SCC)
- Compute Engine / Snapshots
- Cloud Storage IAM
- VPC Firewall Rules
- Cloud Logging

## Report
Full incident response report included in this repo.

# Repo contents:

```js
gcp-incident-response-lab/           
├── README.md                                            
├── Cymbal_Retail_Incident_Response_Report.pdf                                 
└── screenshots/                                                    
    ├── attacks.png                                   
    ├── deleting_default_firewall_rules.png                               
    ├── PCI_DSS.png                                      
    ├── permisson_mangement.png                                         
    ├── vm_config.png
    ├── vm_restoration.png
    ├── vuln2.png               
    ├── vulns1.png                                                     
    └── vm_redeployement.png                                                                 
```