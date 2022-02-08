# Exploit Prediction Scoring System (EPSS) Catalog Enrichment

The [Exploit Prediction Scoring System (EPSS)](https://www.first.org/epss/) is an open, data-driven effort for estimating the likelihood (probability) that a software vulnerabilities will be exploited in the wild. Our goal is to assist network defenders to better prioritize vulnerability remediation efforts.

The data they provide is minimal, so I have built this jupyter notebook to enrich the data using the data feeds from the [NVD](https://nvd.nist.gov/)  to create a CSV and JSON file that containes the following data points:

- CVE
- EPSS
- CVSS_V3
- BaseSeverity
- CWE
- Scope
- AttackVector
- AttackComplexity
- PrivilegesRequired
- UserInteraction
- Description
- Published

A Github Action runs every 6 hours and updates the following files:

- [epss_enriched.csv](epss_enriched.csv)
- [epss_enriched.json](epss_enriched.json)
