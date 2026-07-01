###  **1. Log Analysis: Top 10 Most Frequent Error Messages**
**Goal**: Extract error messages from logs, clean them, and rank by frequency.
```bash
grep "ERROR" /var/log/app.log | sed 's/^.*ERROR: //' | awk '{count[$0]++} END {for (msg in count) print count[msg], msg}' | sort -nr | head -10
```
- `grep` filters lines containing "ERROR".
- `sed` strips everything before the error message.
- `awk` counts occurrences of each unique message.
- `sort` ranks by frequency.

---

###  **2. Web Logs: Top 10 IPs by Request Count**
**Goal**: Identify the most active IPs in Nginx/Apache logs.
```bash
grep -E '^[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+' /var/log/nginx/access.log | sed 's/ .*//' | awk '{count[$0]++} END {for (ip in count) print count[ip], ip}' | sort -nr | head -10
```
- `grep` matches lines starting with an IP.
- `sed` keeps only the IP (removes everything after the first space).
- `awk` counts requests per IP.

---

###  **3. Email Extraction: Count Emails by Domain**
**Goal**: Extract all emails from files and count occurrences by domain.
```bash
find /var/www -type f -name "*.html" -exec grep -oE '\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}\b' {} + | sed 's/.*@//' | awk '{count[$0]++} END {for (domain in count) print count[domain], domain}' | sort -nr
```
- `grep -oE` extracts email addresses.
- `sed` strips the local part, leaving only the domain.
- `awk` counts domains.

---

###  **4. Code Analysis: Most Called Functions in Python Files**
**Goal**: Find the most frequently called functions in a codebase.
```bash
find src/ -name "*.py" -exec grep -oE '\b([a-zA-Z_][a-zA-Z0-9_]*)\s*\([^)]*\)' {} + | grep -v "^def\|^class\|^import" | sed 's/(.*//' | awk '{count[$0]++} END {for (func in count) print count[func], func}' | sort -nr | head -20
```
- `grep` matches function calls (e.g., `func()`).
- `grep -v` excludes definitions (`def`, `class`, `import`).
- `sed` removes arguments, leaving only the function name.
- `awk` counts calls per function.

---

###  **5. Text Processing: Word Frequency (Case-Insensitive)**
**Goal**: Analyze word frequency in a document, ignoring case.
```bash
cat novel.txt | grep -oE '\b[a-zA-Z]+\b' | sed 's/.*/\L&/' | awk '{count[$0]++} END {for (word in count) print count[word], word}' | sort -nr | head -50
```
- `grep -oE` extracts individual words.
- `sed \L` converts words to lowercase.
- `awk` counts occurrences.

---

###  **6. System Monitoring: CPU Usage by Process**
**Goal**: Calculate total CPU usage per process name.
```bash
ps aux | grep -v "grep" | sed 's/  */|/g' | awk -F'|' '{cpu[$11]+=$3} END {for (proc in cpu) print proc, cpu[proc]}' | sort -nr -k2
```
- `ps aux` lists all processes.
- `sed` replaces whitespace with pipes for cleaner parsing.
- `awk` sums CPU usage (`$3`) per process name (`$11`).

---

###  **7. Nginx Logs: Response Time Statistics**
**Goal**: Calculate average, min, and max response times from logs.
```bash
grep -oE 'response_time=[0-9.]+' /var/log/nginx/access.log | sed 's/response_time=//' | awk '{sum+=$1; count++; if($1>max) max=$1; if($1<min || min=="") min=$1} END {print "Avg:", sum/count, "Min:", min, "Max:", max}'
```
- `grep` extracts `response_time=X.XX` values.
- `sed` removes the prefix.
- `awk` computes statistics.

---

###  **8. Data Cleaning: Standardize Phone Numbers**
**Goal**: Extract phone numbers, remove formatting, and deduplicate.
```bash
grep -oE '\b[0-9]{3}[-.]?[0-9]{3}[-.]?[0-9]{4}\b' contacts.txt | sed 's/[^0-9]//g' | awk '{print substr($0,1,3)"-", substr($0,4,3)"-", substr($0,7)}' | sort -u
```
- `grep` matches phone numbers in various formats.
- `sed` removes all non-digit characters.
- `awk` reformats as `XXX-XXX-XXXX`.
- `sort -u` deduplicates.

---

###  **9. Security: Failed SSH Login Attempts by IP**
**Goal**: Identify IPs with the most failed SSH login attempts.
```bash
grep "Failed password" /var/log/auth.log | sed 's/.*from //;s/ port.*//' | awk '{count[$0]++} END {for (ip in count) print count[ip], ip}' | sort -nr
```
- `grep` filters failed login lines.
- `sed` extracts the IP address.
- `awk` counts failures per IP.

---
---
###  **10. CSV Processing: Extract, Transform, and Reformat**
**Goal**: Extract columns from a CSV, apply a transformation, and reformat.
```bash
cat inventory.csv | grep -v "^#" | sed 's/ //g' | awk -F',' '{print $1, $3*1.2, $5}' | sed 's/ /|/g'
```
- `grep -v "^#"` skips comment lines.
- `sed` removes spaces for consistency.
- `awk` extracts columns 1, 3 (with 20% markup), and 5.
- `sed` replaces spaces with pipes for a custom format.