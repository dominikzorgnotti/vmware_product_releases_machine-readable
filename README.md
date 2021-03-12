# Machine-readable VMware release data

This repo contains the release data of VMware products in a machine-readable format (currently JSON). It enables you to use the data easier in scripts or other automation use-cases.  
The data is generated by a GitHub action running daily from [my transformation script](https://github.com/dominikzorgnotti/transform-vmware-product-builds-to-json).  

## Data standardization
Since v0.1.0 of the transformation script the raw data from the published KB is transformed to establish a standard in terms of column headers, formatting, etc.

## Output format and folder structures
Different use-cases, different ways to organize data.  
The way the output is currently structured is:   
- Directory: based on Pandas options to handle [json data orientation](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_json.html)
    - Files: KB(a)_(b)_table(c)_release_as_(d)"
       - a: knowledge base article id - the unique ID for the KB article
       - b: product name - The first product from the meta data, all in lower case and spaces replaced by underscores
       - c: An id to identify multiple html tables on the section (starting at 0)
       - d: json data orientation - see above

I will try to maintain a stable folder structure and data output formats but reserve the right to change it at any time.

## Source
Please review the original source of data [Correlating build numbers and versions of VMware products (1014508)](https://kb.vmware.com/s/article/1014508?lang=en_US)

| Product name	| Article |
:-----:|:-----:
VMware Converter Standalone	| Build numbers and versions of VMware Converter Standalone (2143828) |
VMware Data Recovery | Build numbers and versions of VMware Data Recovery (2143852) |
VMware ESXi/ESX | Build numbers and versions of VMware ESXi/ESX (2143832) |
VMware Horizon View | Build numbers and versions of VMware Horizon View (2143853) |
VMware NSX for vSphere | Build numbers and versions of VMware NSX for vSphere (2143854) |
VMware Site Recovery Manager | Build numbers and versions of VMware Site Recovery Manager (2143851) |
VMware vCenter Server | Build numbers and versions of VMware vCenter Server (2143838) |
VMware vCenter Chargeback | Build numbers and versions of VMware vCenter Chargeback (2143841) |
VMware vCloud Connector | Build numbers and versions of VMware vCloud Director and VMware vCloud Connector (2143847) |
VMware vCloud Director | Build numbers and versions of VMware vCloud Director and VMware vCloud Connector (2143847) |
VMware vCloud Networking and Security | Build numbers and versions of VMware vCloud Networking and Security (2143848) |
VMware vRealize Automation | Build numbers and versions of VMware vRealize Automation (2143850) |
VMware vRealize Orchestrator | Build numbers and versions of VMware vRealize Orchestrator (2143846) |
VMware vRealize Operations Manager | Build numbers and versions of VMware vRealize Operations Manager (2145975) |
VMware vSAN	| Build numbers and versions of VMware vSAN (2150753) |
VMware vShield | Build numbers and versions of VMware vShield (2143849) |
VMware vSphere Update Manager	| Build numbers and versions of VMware vSphere Update Manager (2143837) |
VMware vSphere Replication Appliance | Build numbers and versions of VMware vSphere Replication Appliance (2143840) |
VMware vSphere Storage Appliance | Build numbers and versions of VMware vSphere Storage Appliance (2145727) |
VxRAIL | Correlating VxRAIL Release with VMware build numbers (52075) |
VMware Cloud Foundation | Correlating VMware Cloud Foundation version with the versions of its constituent products (52520) |
VMware vRealize Network Insight (vRNI) | Build numbers and versions of VMware vRealize Network Insight (67245) |

Based on feedback: I can only with data that is published in the KB articles. It may not include pulled releases or beta builds.

## Disclaimer

This is not an official VMware repository. It is not linked in any capacity to my employment at VMware.    
All data that is processed is provided by VMware. I am just transforming the data VMware publishes in the knowledgebase and provide them in a different output format.
Errors can and will be made, please us this at your own discretion and test it out.
