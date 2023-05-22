# Snowflake Cloud Platforms

* Snowflake can be hosted on any of the below:
    - AWS
    - MS Azure
    - GCP
* It provides more regions on each platform
* If we already have services hosted on any of the above platform then Snowflake can host on the same platform or different platform can also be chosen
* Example
    - SF Account 1 => Hosted on AWS
    - SF Account 2 => Hosted on Azure
    - Both accounts are possible and independent to each other though both are managed by you and differs a bit with billing part

## Security Certification => HITRUST CSF
* Enhances the security posture in regulatory compliance and risk management
* Applicable to editions Business Critical and Higher

## Limitations for Accounts on GCP
* No support to 2 use cases
    1. Cross-region private connectivity
    2. On-premises connection to Snowflake
* Possible workaround - Creating a proxy forma and routing it to forwarding rule where the Google Cloud connecting must be in same region
* No support for Snowflake system functions for self-service management
    - SYSTEM$AUTHORIZE_PRIVATELINK
    - SYSTEM$REVOKE_PRIVATELINK
    - SYSTEM$GET_PRIVATELINK
    - SYSTEM$GET_PRIVATELINK_AUTHORIZED_ENDPOINTS
* No support for private connectivity to Internal Stages
(Primarily intended for administrator roles like ACCOUNTADMIN, SYSADMIN, SECURITYADMIN)

## Limitations for accounts on Azure
* Currently, using account name URL format not supported, use Account Locator format (For: SnowSQL, Connectors, Drivers)
* Snowflake hosted on Azure supports the below given third-party application
    - Attunity
    - Databricks
    - Fivetran
    - Informatica
    - Looker
    - Matillion
    - Microstrategy
    - Periscope
    - Power BI
    - Qubole
    - Sigma Computing
    - Stitch
    - Tableau
    - Talend
    - Wherescape
