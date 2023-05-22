# Snowflake supported Cloud Regions

## Why regions are important ?
* It let's to choose where the data is geograhically stored across regional, national, international operations
* Also, used to determine where the compute resources are provisioned
* Grouped into 3 global segments:
    1. North & South America
    2. Europe & Middle East
    3. Asia Pacific
* Only 1 Snowflake Account per Region (1 SF a/c =>  1 Region)

## Points to Note

- There are no restrictions to choose region during the Snowflake account creation
- Regions do not limit user access to Snowflake (they only dictate the grographic location where the data is stored & compute resources are provisioned)
- Snowflake do not move the data between accounts
- There are 2 formats in Snowflake Account Hostname   
    1. Account Name (Preferred)
    2. Account Locator (includes cloud region & platform)
- URL starts with account hostname and ends with Snowflake domain name which is snowflakecomputing.com
