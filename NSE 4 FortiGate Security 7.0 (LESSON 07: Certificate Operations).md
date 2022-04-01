**Which attribute or extension identifies the owner of a certificate?**

- The subject name in the certificate
- ~~The unique serial number in the certificate~~

**How does FortiGate determine if a certificate has been revoked?**

- It checks the CRL that resides on FortiGate
- ~~It retrieves the CRL from a directory server~~

**Which certificate extension and value is required in the FortiGate CA certificate in order to enable full SSL inspection?**

- ~~CRL DP=ca_arl.arl~~
- cA=True

**Which configuration requires FortiGate to act as a CA for full SSL inspection?**

- Multiple clients connecting to multiple servers
- ~~Protecting the SSL server~~

**Which CSR enrollment method is supported by FortiGate?**

- ~~Enrollment over Secure Transport (EST)~~
- Simple Certificate Enrollment Protocol (SCEP)

|||
| --- | --- |
| Enrollment Method | Online SCEP: the Simple Certificate Enrollment Protocol (SCEP) allows devices to enroll for a certificate by using a URL and a password. The SCEP server works as a proxy to forward the FortiGate’s request to the CA and returns the result to the FortiGate (setting up an SCEP server is beyond the scope of this topic). Once the request is approved by the SCEP server, the FortiGate will have a signed certificate containing the details provided in the CSR. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/322226/uploading-a-certificate-using-the-gui

**After a CSR has been enrolled and imported into FortiGate, the status of the certificate should change to:**

- Valid
- ~~Pending~~
