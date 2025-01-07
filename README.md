# Reverse Shells Collection

This repo contains a set of php reverse shell scripts. They are used for connecting back to an attacker’s machine over a TCP connection. Once the connection is made, the attacker gets access to a shell with the same privileges as the user running the web server.

**⚠️ Legal Disclaimer:**  
These scripts are **ONLY** for educational purposes and **authorized penetration testing**. Do not use them for unauthorized activities. Using these scripts without permission may be illegal. Always get explicit authorization before testing any systems.

---

## How to Use

### 1. Set up a listener on your machine
On your attacking machine, start a **netcat listener** to wait for the reverse shell connection.

```bash
nc -lvnp 1234
```

### 2. Upload the PHP Script
Upload the desired PHP reverse shell script to the target server. This can be done via a web shell, file upload vulnerability, or any other method depending on your test scenario.

### 3. Execute the Script
Once the file is uploaded, access it through a browser (e.g., `http://target.com/shell.php`), and you’ll get a remote shell on your machine.

---

## Customization

Each of these scripts requires you to set your attacker's IP address and port. Edit the following lines in the script:

```php
$ip = '127.0.0.1';  // Change this to your attacker's IP
$port = 1234;       // Change this to your chosen port
```

---

## Important Notes

- These scripts are meant for **authorized** penetration testing **only**. Do not test systems without permission.
- If you're running this on a live server, make sure you're aware of any potential risks and legal consequences.
- The reverse shell will typically run with the same privileges as the web server user (often `www-data`), so the permissions will be limited.
- For success, ensure the target server allows outbound connections and the firewall isn't blocking your connection.

---

Happy hacking (responsibly)! 😎
