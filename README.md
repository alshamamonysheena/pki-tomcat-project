# PKI & Tomcat HTTPS Deployment

This project sets up a full PKI system with OpenSSL and uses it to secure a Tomcat web server with a TLS certificate.

## What I Did

- ✅ Created a Root CA and Signing CA using OpenSSL
- ✅ Issued a TLS certificate for `www.simple.org`
- ✅ Bundled the certificate and key into a `.p12` file
- ✅ Installed and configured Tomcat 11 via Homebrew on macOS
- ✅ Configured `server.xml` to use the TLS cert on port 8443
- ✅ Added `www.simple.org` to `/etc/hosts`
- ✅ Trusted the Root CA in macOS Keychain
- ✅ Verified working HTTPS at `https://www.simple.org:8443`

## Folder Structure

```
pki-example-1/
├── ca/
│   ├── root-ca/
│   └── signing-ca/
├── certs/
├── etc/
├── crl/
```

## How to Test

1. Add to `/etc/hosts`:
   ```
   127.0.0.1 www.simple.org
   ```
2. Visit: `https://www.simple.org:8443`
3. Trust the root CA to avoid browser warnings

## Author

**Alshama**  
CMPE 272 – May 2025
