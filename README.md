# CWE-AI

This code is used to build a machine learning model that can predict the category of a software vulnerability based on its name. The categories are called CWEs, and they are assigned a number and are useful to determine phases, generic remediation and impact related to such software vulnerability / weakness.

The dataset (tagged_cve_cwe.tsv) was built by scraping Snyk Database and the official NIST CVE Data Feeds:

- Titles of Vulnerabilities gathered from Snyk Database
- CVE from the Vulnerability
- NVD Descriptions are also on a column in case you want to use them.
- CWE that matches the CVE (in case there are many, we use the first one).

To see an step by step tutorial on how to do this, open README.ipynb

#### Final result

```
# Good Titles
guess_cwe('Structured Query Language Injection')
guess_cwe('SQL Injection')
guess_cwe('Double Free')
guess_cwe('Use After Free')
guess_cwe('OS CMD Injection')
guess_cwe('Denial of Service')
# Random Stuff
guess_cwe('Donald Trump')
guess_cwe('Mechanical Confusion')
guess_cwe('Static Analysis')

The predicted score for Structured Query Language Injection (CWE-89): 40.97%
The predicted score for SQL Injection (CWE-89): 94.04%
The predicted score for Double Free (CWE-415): 94.94%
The predicted score for Use After Free (CWE-416): 93.36%
The predicted score for OS CMD Injection (CWE-78): 75.20%
The predicted score for Denial of Service (CWE-400): 66.35%
The predicted score for Donald Trump (CWE-416): 7.84%
The predicted score for Mechanical Confusion (CWE-416): 7.84%
The predicted score for Static Analysis (CWE-416): 7.84%
