# CWE-AI

This code is used to build a machine learning model that can predict the category of a software vulnerability based on its name. The categories are called CWEs, and they are assigned a number and are useful to determine phases, generic remediation and impact related to such software vulnerability / weakness.

The dataset (tagged_cve_cwe.tsv) was built by scraping Snyk Database and the official NIST CVE Data Feeds:

- Titles of Vulnerabilities gathered from Snyk Database
- CVE from the Vulnerability
- NVD Descriptions are also on a column in case you want to use them.
- CWE that matches the CVE (in case there are many, we use the first one).

To see an step by step tutorial on how to do this, open README.ipynb
