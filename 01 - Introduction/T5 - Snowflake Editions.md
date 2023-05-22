# Snowflake Editions

* Snowflake offers multiple editions to choose from, ensuring that usage fitting our requirements
* When needs change/grow, changing editions is easy
* Editions determines the unit costs for the credits and the database storage used
* Other important factors impacting unit costs are
    1. Region (selected)
    2. Account Type
        * On-Demand: Usage-based pricing with no long-term licensing requirements
        * Capacity: Discounted pricing based on an up-front capacity committment

## Types of Editions

1. **Standard Edition**
    - Introductory level offering
    - Provides full, unlimited access to all Snowflake features
    - Strong balance between features, level of support cost
    - Complete SQL datawarehouse
    - Secure data sharing across regions/clouds
    - Support: 24 x 365
    - Time Travel: 1 Day
    - Encryption: Always on enterprise grade (in-transit & at rest)
    - Customer-dedicated virtual warehouses
    - Federated Authentication
    - Supports Database replication, External Functions
    - Creates own data exchange
    - Access to data marketplace

2. **Enterprise Edition**
    - Standard Edition **+**
    - Additional features for neds of large-scale enterprises and organizations
    - Multi-cluster warehouse
    - Time Travel: 90 Days
    - Encrypted data: Annual Rekeying
    - Materialized Views
    - Search Optimization Service
    - Dynamic data masking
    - External data tokenization


3. **Business Critical**
    - Enterprise Edition **+**
    - Also known as *Enterprise for Sensitive Data* (ESD)
    - Offers higher level of data protection to support with extremely sensitive data
    - Especially for PHI data: complies with HIPAA & HITRUST CSF regulation
    - For any PHI data to store in Snowflake: (BAA) Signed Business Associate Agreement must be between the organization and Snowflake inc
    - Database failover/failback adds support for business continuity and disaster recovery
    - So, HIPAA supports and PCI Compliance
    - Tri-secret secure using customer managed keys
    - AWS & Azure private link support
    - GCP private connect support
    - External Functions: Has AWS API gateway and private endpoints support

4. **Virtual Private Snowflake (VPS)**
    - Business Critical Edition **+**
    - Offers highest level of security for strictest requirements such as financial institutions with highly sensitive data
    - Completely separate SF environment (Isolated from all other SF accounts)
    - VPS accounts do not share any resources with accounts outside VPS
    - If still need to share the data to non-VPS, contact Snowflake to enable the listing autofillment
    - Account Locator format: different from other SF editions
    - Customer-dedicated virtual servers (wherever encryption keys in memory)
    - Customer-dedicated metadata store
