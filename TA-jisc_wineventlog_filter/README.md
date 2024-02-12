# Purpose

*This is for UF only.*

Mitigate risk of splunk management commands being issued from a remote machine.

This app changes the accessibility to the management port for universal forwarders. Also disables the web interface.

## Notes

Splunk's complete mitigation suggests:

1. Certificates on management ports.

   The intermediate forwarders have certificates talking to the remove servers.
   
2. Disabling binding to the management port in splunk-launch.conf

   This is difficult to do since requires updating each machine separately. Might as well update the forwarder to version 9.

## References

https://www.splunk.com/en_us/product-security/announcements/svd-2022-0605.html?_gl=1*1oucq2a*_ga*MjMyMTc1NDI5LjE1ODM3NjkzMTU.*_gid*MTgzOTA1MTgzNy4xNjU3MTg1NDYz&_ga=2.65134254.1839051837.1657185463-232175429.1583769315
https://docs.splunk.com/Documentation/Splunk/9.0.0/Security/EnableTLSCertHostnameValidation#Configure_TLS_host_name_validation_for_the_Splunk_CLI
https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-32156
