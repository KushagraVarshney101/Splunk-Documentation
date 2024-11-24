# Splunk Internal Pen Testing or Security Tools Search Queries

1. **Find instances of Nmap port scans**:
   ```spl
   index=* sourcetype=*
   | search "Nmap"
   | table _time, src_ip, dest_ip, port, protocol
   ```

2. **Detect use of Metasploit Framework**:
   ```spl
   index=* sourcetype=*
   | search "Metasploit"
   | table _time, src_ip, dest_ip, exploit, payload
   ```

3. **Identify SQL injection attempts**:
   ```spl
   index=* sourcetype=*
   | regex ".(UNION ALL|SELECT\s+*).(FROM|WHERE).*(--|;)"
   ```

4. **Look for brute force attacks using Hydra**:
   ```spl
   index=* sourcetype=*
   | search "Hydra"
   | table _time, src_ip, dest_ip, user, password_attempt
   ```

5. **Search for usage of the Wireshark packet sniffer**:
   ```spl
   index=* sourcetype=*
   | search "Wireshark"
   | table _time, src_ip, dest_ip, protocol, packet_info
   ```

6. **Detect use of the Mimikatz tool for credential dumping**:
   ```spl
   index=* sourcetype=*
   | search "Mimikatz"
   | table _time, src_ip, dest_ip, username, password
   ```

7. **Discover instances of the Nikto web vulnerability scanner**:
   ```spl
   index=* sourcetype=*
   | search "Nikto"
   | table _time, src_ip, dest_ip, vulnerability, severity
   ```

8. **Identify the use of the Burp Suite web application security testing tool**:
   ```spl
   index=* sourcetype=*
   | search "Burp Suite"
   | table _time, src_ip, dest_ip, request, response
   ```

9. **Detect instances of the Nessus vulnerability scanner**:
   ```spl
   index=* sourcetype=*
   | search "Nessus"
   | table _time, src_ip, dest_ip, vulnerability, severity
   ```

10. **Find use of the John the Ripper password cracker**:
   ```spl
   index=* sourcetype=*
   | search "John the Ripper"
   | table _time, src_ip, dest_ip, hash, password_attempt
   ```
