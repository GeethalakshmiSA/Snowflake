# Some important notes

1. **Query History Page** displays all the SQL Statements executed in **last 14 days**
2. **Client Info** column indicates the Snowflake Client Version
3. Snowflake updates the info on which versions are supported - For **Every 3 months**
4. SnowCD (Snowflake Connectivity Diagnostic Tool) => Used to diagnose and troubleshoot their network connection to Snowflake
5. For connection check & troubleshoot network connection to Snowflake, use below functions:
    - *SYSTEM$ALLOWLIST()*
    - *SYSTEM$ALLOWLIST_PRIVATELINK()*
6. SnowCD works with **direct connection** and **through proxy servers**
7. SnowCD detects problems like
    - No HTTP server running in specified IP address and port
    - DNS lookup failure
    - Man-in-the-middle attack
    - Invalid certificate to impersonate desired service
    - Other network failures below HTTP level
8. SnowCD does not perform a strict check on HTTP response from a Stage
9. SnowCD does not detect problems like
    - Access policy denial for AWS/Azure BLOB/GCP stages
    - Connection to proxy server (403 error)
10. Currently, Snowflake does not support SSL-terminating proxy servers
11. SnowCD supports the full description on flags => execute *snowcd -h*
12. Hostnames allowed depends on **Cloud platform (AWS/Azure/GCP)** and **Region where the account is located**
13. Limit of size of query test which includes string/binary literals (part of WHERE/SET clause) => **1 MB per statement**
14. Snowflake compresses data when sending it between client & server
15. Limit applies to size **AFTER compression** (So, keep the uncompressed size within the limit)
16. OCSP *(Online Certificate Status Protocol)* provides maximum security determining whether a certificate is revoked when Snowflake 
client attempts to connect endpoint through HTTPS
18. Snowflake uses OCSP to evaluate the root certificate authority (RCA)
19. OCSP CA response has 2 behaviors
    * Fail-open
        - Indicating revoked certificate results in failed connection
        - Denotes the logs of other certificate errors at WARNING level in JSON format
        - No support for OCSP checking for .NET driver
    * Fail-close
        - If OCSP CA respnse is not valid, the connection fails
        - Must be configured manually with each driver/connector
        - To preserve this behavior, set OCSP_FAIL_OPEN = false
19. For most accounts in US West (AWS) - Snowflake uses digicert-signed certificates from network solutions
20. For other regions (AWS), Snowflake uses certificates from Amazon CA
21. All communication with Snowflake happens using 443 port
22. However, OCSP certification are transmitted over port 80
23. CRL (Cerificate Revocation List) specifies the certificates explicitly revoked by CA
24. Some drivers/connectors support ability to send SQL statements like SELECT, DML commands, SHOW to prepare before execution and others not prepare before execution
