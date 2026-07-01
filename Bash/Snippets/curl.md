# GENERAL USAGE
```bash
# Check Weather
curl http://wttr.in/atlanta

# Check current IP
curl ipinfo.io
curl -s http://whatismyip.akamai.com
curl -s icanhazip.com

# Website Status
curl -Is https://www.twitter.com -L | grep HTTP/
curl https://www.twitter.com -m 5 -s -f -o /dev/null && echo "SUCCESS" || echo "UNREACHABLE"
```

* Send mail using curl
```bash
echo "To:receiver@gmail.net" > /tmp/mail.txt
echo "Subject:test" >> /tmp/mail.txt
echo "This is a test" >> /tmp/mail.txt

curl --url "smtps://smtp.gmail.com:465" --ssl-reqd --mail-from "sender@gmail.com" --mail-rcpt "receiver@gmail.net"   --upload-file /tmp/mail.txt --user "sender@gmail.com:sender_pass" --insecure

rm /tmp/mail.txt
```

# POST

* PushBullet API
```bash
# create push
access_token="o.blahblahblah"
body="text content"
title="title"
email="something@gmail.com"

curl --header 'Access-Token: $access_token' \
     --header 'Content-Type: application/json' \
     --data-binary '{"body":"'" $body"'","title":"'"$title"'","type":"note","email":"'"$email"'"}' \

     --request POST \
     https://api.pushbullet.com/v2/pushes

```

### **Resume a Partially Downloaded File**
**Goal**: Continue a failed download from where it left off.
```bash
curl -C - -O https://example.com/largefile.zip
```
- `-C -` tells curl to auto-resume based on the local file's size.
- `-O` saves the file with its original name.

---

### **Upload a File with Multipart Form Data**
**Goal**: Upload a file with additional form fields (e.g., for REST APIs).
```bash
curl -F "file=@/path/to/report.pdf;filename=annual_report.pdf" \
     -F "title=Annual Report 2026" \
     -F "author=John Doe" \
     -F "category=finance" \
     https://example.com/api/upload
```
- `-F` sends multipart form data.
- `@/path/to/file` uploads the file.
- `filename=...` overrides the uploaded filename.

---

### **API Request with Bearer Token & Custom Headers**
**Goal**: Authenticate with OAuth 2.0 and send custom headers.
```bash
curl -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
     -H "Content-Type: application/json" \
     -H "X-API-Version: 2.0" \
     -H "X-Request-ID: $(uuidgen)" \
     https://api.example.com/protected/resource
```
- `-H` adds custom headers.
- `uuidgen` generates a unique request ID (Linux/macOS).

---

### **Download Multiple Files Using URL Globbing**
**Goal**: Download a sequence of files with a single command.
```bash
curl -O https://example.com/images/[001-100].jpg
```
- `[001-100]` expands to `001.jpg`, `002.jpg`, ..., `100.jpg`.
- `-O` saves each file with its original name.

---

### **Send a JSON POST Request from a File**
**Goal**: Send structured JSON data from a file to an API.
```bash
curl -X POST \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     --data @payload.json \
     https://api.example.com/endpoint
```
- `-X POST` sets the HTTP method.
- `--data @payload.json` reads the JSON body from a file.

---

### **Use a SOCKS5 Proxy with Authentication**
**Goal**: Route traffic through a SOCKS5 proxy (e.g., Tor, SSH).
```bash
curl --socks5 proxy.example.com:1080 \
     -U proxyuser:proxypass \
     https://example.com
```
- `--socks5` specifies the proxy host and port.
- `-U` provides proxy credentials.

---

### **Session Persistence with Cookies**
**Goal**: Maintain a login session across multiple requests.
```bash
# Step 1: Login and save cookies
curl -c session_cookies.txt \
     -u username:password \
     https://example.com/login

# Step 2: Use saved cookies for authenticated requests
curl -b session_cookies.txt \
     https://example.com/dashboard
```
- `-c` saves cookies to a file.
- `-b` sends cookies from a file.

---

### **Rate-Limited Download with Progress Bar**
**Goal**: Download a large file at a controlled speed (e.g., 1MB/s).
```bash
curl --limit-rate 1M \
     --progress-bar \
     -O https://example.com/largefile.iso
```
- `--limit-rate 1M` caps the download speed at 1 megabyte per second.
- `--progress-bar` shows a visual progress indicator.

---

### **Get Detailed Timing Breakdown**
**Goal**: Measure DNS, TCP, TLS, and total request time for performance testing.
```bash
curl -o /dev/null \
     -s \
     -w "DNS: %{time_namelookup}s\nTCP: %{time_connect}s\nTLS: %{time_appconnect}s\nTotal: %{time_total}s\n" \
     https://example.com
```
- `-o /dev/null` discards the output.
- `-w` writes custom timing metrics to stdout.

---
---
### **Mutual TLS (mTLS) with Client Certificates**
**Goal**: Authenticate with a server using client-side certificates.
```bash
curl --cert client.crt \
     --key client.key \
     --cacert ca.crt \
     https://mtls.example.com/secure
```
- `--cert` specifies the client certificate.
- `--key` specifies the private key.
- `--cacert` specifies the CA certificate for server verification.