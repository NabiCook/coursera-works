# Coursera: Google Cybersecurity Professional Certificate

This repository contains my projects, scripts, and reports from the Google Cybersecurity Professional Certificate program on Coursera. The work below demonstrates my hands-on skills in Python automation, Linux/SQL, network security, and security data analysis.

---

## Featured Projects & Skills

### Automating Cybersecurity Tasks with Python

This module focused on using Python to automate common security operations. The scripts demonstrate file handling, hashing, and interacting with APIs.

* **Example: Hashing a file to verify integrity**
    This script calculates the SHA256 hash of a file, a common task for verifying file integrity against known threats.

    ```python
    # From: hash_file.py
    import hashlib

    def hash_file(filename):
        """This function returns the SHA-256 hash of the file passed into it"""
        h = hashlib.sha256()
        with open(filename, 'rb') as file:
            chunk = 0
            while chunk != b'':
                chunk = file.read(1024)
                h.update(chunk)
        return h.hexdigest()

    message = hash_file("track.mp3")
    print(message)
    ```

[**Browse the Python scripts here.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity/Automating-Cybersecurity-Tasks-with-Python)

---

### Linux and SQL for Cybersecurity

This section showcases the use of essential Linux command-line tools and SQL queries for log analysis, file system auditing, and database inspection.

* **Example: Linux Command**
    Using `grep` to search for failed login attempts in an authentication log file.
    ```bash
    grep "Failed password" /var/log/auth.log
    ```

* **Example: SQL Query**
    Querying a database to identify all employees in the 'Sales' department who have administrative access.
    ```sql
    SELECT e.username, e.role
    FROM employees e
    JOIN departments d ON e.department_id = d.id
    WHERE e.role = 'admin' AND d.name = 'Sales';
    ```

[**See more from this module here.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity/Linux_and_SQL)

---

### Security Data Analysis: SPL and Regex

This project involved using Splunk Processing Language (SPL) and Regular Expressions (Regex) to search, filter, and analyze security data from logs.

* **Example: Splunk (SPL) Query**
    An SPL query to find the top 10 source IP addresses responsible for failed login attempts.
    ```spl
    eventtype=authentication action=failure
    | top limit=10 src_ip
    ```

* **Example: Regex Filter**
    A Regex pattern designed to identify and extract any valid email addresses from a block of text.
    ```regex
    [a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}
    ```

[**View the filters and queries here.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity/spl_and_regex_filters)

---

### Network Analysis and Security

This section focused on analyzing network traffic to identify protocols, anomalies, and potential security threats. The work involved inspecting packet captures (`.pcapng` files) using tools like Wireshark and tcpdump. The analysis reports summarize findings from these captures.

[**Explore the network analysis files here.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity/Networks_and_Network_Security)

---

### Security Frameworks, Risk, and Incident Response

This part of the certificate program involved written analyses and reports on core cybersecurity concepts. The documents cover:
* **Risk Management:** Identifying and assessing assets, threats, and vulnerabilities.
* **Security Frameworks:** Applying standards like the NIST Cybersecurity Framework to improve security posture.
* **Incident Response:** Developing plans for detecting and responding to security incidents.

[**Read the reports here.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity)