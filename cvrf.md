# Project Title

Python OpenVulnAPI Alternative

## Getting Started

This project will enable you to make api calls to get security advisories of cvrf.

## Config File

You need to have a cred.json file in which you need to store your credentials in Json Format like this:

```
{	
	"client_id":"",
	"client_secret":"",
}

```
Its Path should be the same as that of the project.


### Prerequisites


You just need to have Python installed. Run below command to install Python. You can download that from this link.

```
https://www.python.org/
```

## Running the tests

Currently only CVRF advisory type is implemented.

API Call will be
```
filename.py --Advisory Type --API Filters <filter_input> --details(OPTIONAL)
```

Advisory Type:

```
--cvrf
        Filter openVuln API by only cvrf advisories
```

API FILTERS:

```
--all
        Return all advisories in cvrf format
        Examples:
        >> openVulnQuery --cvrf --all

--advisory
        Search by specific advisory id
        Examples:
        >> openVulnQuery --cvrf --advisory cisco-sa-20110201-webex

--cve
        Search by specific cve id
        Examples:
        >> openVulnQuery --cvrf --cve CVE-2010-3043

--latest
        Search by the number of latest advisories in cvrf format
        Examples:
        >> openVulnQuery --cvrf --latest 10

        Note: the latest option is limited to 100 maximum queries

--severity
        Search by severity (low, medium, high, critical)
        Note: Oval does not have a low severity
        Examples:
        >> openVulnQuery --cvrf --severity critical
        >> openVulnQuery --cvrf --severity high
        >> openVulnQuery --cvrf --severity medium
        >> openVulnQuery --cvrf --severity low

--year
        Search by the year (1995 to present)
        Examples:
        >> openVulnQuery --cvrf --year 2016

--product
         Search by the product name
         Examples:
         >> openVulnQuery --cvrf --product Cisco

```
	
