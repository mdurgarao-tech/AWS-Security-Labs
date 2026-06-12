# AWS Security Labs

Hands-on labs securing AWS cloud workloads — VPC and subnet design, network access controls (Security Groups & NACLs), least-privilege IAM, route tables, and logging/monitoring. Focused on applying defense-in-depth and least-privilege principles to cloud networking.

This repo documents practical AWS security work I've done as a Network Security Engineer extending network security controls into the cloud.

---

## What's covered

### VPC & Network Design
- Designed VPCs with public and private **subnets** across availability zones.
- Planned CIDR ranges and segmentation to isolate workloads by tier and trust level.

### Network Access Controls
- **Security Groups** — instance-level, stateful rules following least-privilege (only required ports/sources).
- **Network ACLs** — subnet-level, stateless rules as an additional layer of control, including explicit deny rules.
- Documented the difference and the layering of SG (stateful) vs NACL (stateless) in a defense-in-depth model.

### Identity & Access Management (IAM)
- Built **least-privilege IAM policies**, scoping permissions to only what each role needs.
- Worked with roles, policy structure (Effect/Action/Resource), and avoiding overly permissive wildcards.

### Routing
- Configured **route tables** for public/private subnet routing, internet gateway and NAT paths, and controlled egress.

### Logging & Monitoring
- Enabled **VPC Flow Logs** and **CloudWatch** to capture traffic and activity for visibility, troubleshooting, and security monitoring.

---

## Topics / Keywords
`AWS` · `Cloud Security` · `VPC` · `Subnets` · `Security Groups` · `NACL` · `IAM` · `Least Privilege` · `Route Tables` · `VPC Flow Logs` · `CloudWatch` · `Defense in Depth` · `Network Security`

---

## Repository structure
```
aws-security-labs/
├── README.md
├── vpc-design/
│   ├── vpc-subnet-notes.md
│   └── diagram/            # add architecture diagram here
├── access-controls/
│   ├── security-groups-notes.md
│   └── nacl-notes.md
├── iam/
│   └── least-privilege-policy-examples.md
└── monitoring/
    └── flow-logs-cloudwatch-notes.md
```

---

## Suggested architecture diagram
A simple diagram to add: **Internet → IGW → Public Subnet (NAT) → Private Subnet (app)**, with Security Groups on instances and NACLs on subnets, and VPC Flow Logs feeding CloudWatch. (You can draw this in draw.io / diagrams.net and export a PNG into `vpc-design/diagram/`.)

---

## Notes
- Labs were built in a personal/test AWS environment. Remove any real account IDs, ARNs, or resource names before publishing.
- IAM policy examples are illustrative — review and scope to your own environment before use.

---

**Author:** Miriyala Durga Rao — Network Security Engineer
[Portfolio](https://mdurgarao-tech.github.io) · [LinkedIn](https://www.linkedin.com/in/miriyala-durgarao)
