# Coursera: Google Cybersecurity Professional Certificate


[![coursera_cert](https://s3.amazonaws.com/coursera_assets/meta_images/generated/CERTIFICATE_LANDING_PAGE/CERTIFICATE_LANDING_PAGE~JXOCGNV0WXXF/CERTIFICATE_LANDING_PAGE~JXOCGNV0WXXF.jpeg)](https://www.coursera.org/account/accomplishments/professional-cert/JXOCGNV0WXXF)

This repository contains my portfolio activities and assignments from the Google Cybersecurity program on Coursera. The work below demonstrates my skills in Python automation, Linux/SQL, network security, and security data analysis.

---

## Featured Projects & Skills

### Automating Cybersecurity Tasks with Python

* **Example: File Update Algorithm**
	```python
	import_file = "allow_list.txt"
	with open(import_file, "r") as file:
		ip_addressess = file.read()
	```
	This code snippet opens the file in read mode `"r"` to access its contents. The `.read()` method loads the file's contents into a single string.
	
	To convert the string of IP addresses into a list, the `.split()` method is used.
	```python
	ip_address.split()
	```
	
	A `for` loop then iterates through each element in the `ip_addresses` list to find matches from a `remove_list`. When a match is found, `.remove()` deletes the entry from the list.
	
	```python
	for element in ip_addresses:
		if element in remove_list:
			ip_addresses.remove(element)
	
	ip_addresses = " ".join(ip_addresses) 	
	```
	The `join()` method then converts the list back into a single string, using a space as a separator, to prepare it for writing back to the file.
	
	```python
	with open(import_file, "w") as file:
		file.write(ip_addresses)
	```
	Finally, the file is opened in write mode "w", and the updated string is saved using `.write()`.

[**View the file.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity/Automating-Cybersecurity-Tasks-with-Python)

---

### Linux and SQL for Cybersecurity

This section showcases the use of essential Linux command-line tools and SQL queries for log analysis, file system auditing, and database inspection.

* **Example: Linux Permission Command**
	The `chmod` command changes file permissions to prevent unauthorized access. Linux shows permissions in User, Group, and Other order, with each having read, write, and execute permissions. For instance, `project_k.txt` has a permission of `-rw-rw-rw-`, which states the user, group, and other users have read and write permissions for the file.
	
	![Linux file permissions](https://raw.githubusercontent.com/NabiCook/coursera-works/main/GoogleCybersecurity/img/Picture1.png)
	
	```bash
	chmod o-w project_k.txt
	```
	The command above uses `-` to remove the write `w` permission from the 'Other' group, making the file read-only for them.

[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/File%20permissions%20in%20Linux.docx)


* **Example: SQL Query**
	This query searches for failed login attempts (1 for success, 0 for fail) that occurred after 6 PM. This is a critical step in identifying suspicious behavior.
	```sql
	SELECT *
	FROM log_in_attempts
	WHERE login_time > '18:00' AND success = 0;
	```
[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/Apply%20filters%20to%20SQL%20queries.docx)

---


### Incident Report Analysis

![Incident Report Sample](https://raw.githubusercontent.com/NabiCook/coursera-works/main/GoogleCybersecurity/img/incident_report.jpg)
> This hands-on activity focused on examining log data from tools like `tcpdump` or Wireshark and detecting suspicious network activity or attacks. In this case, multiple ICMP packets were identified, indicating an ICMP flood (DDoS) attack. The report contains several suggestions to mitigate the risk, such as configuring firewall rules, blocking unused ports, blacklisting IP addresses used for attacks, and installing an IDPS.

[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/Incident%20report%20analysis.docx)

![Data Leak Analysis Sample](https://raw.githubusercontent.com/NabiCook/coursera-works/main/GoogleCybersecurity/img/data_leak.jpg)
> This report covers an incident where a sales manager left access to internal-only files available, resulting in a data leak. After a thorough analysis, suggestions were made to align with NIST SP 800-53 guidelines. Recommendations included implementing a user access timeout and role-based permission controls to prevent unauthorized access. An automatic timeout system would have revoked access to the link before it could be opened, and a permission system would have prevented the external partner from viewing internal-only content.

[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/Activity%20Template_%20Data%20leak%20worksheet.docx)


---

### Risk and Compliance Analysis

![Compliance Checklist Sample](https://raw.githubusercontent.com/NabiCook/coursera-works/main/GoogleCybersecurity/img/compliance.jpg)
> This activity simulated a hands-on security compliance audit. Various criteria were evaluated according to relevant guidelines, such as PCI DSS for payment security and GDPR for EU compliance.

[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/Controls%20and%20compliance%20checklist.pdf)

![Risk Register Sample](https://raw.githubusercontent.com/NabiCook/coursera-works/main/GoogleCybersecurity/img/risk_register.jpg)
> This activity scored and ranked risks according to their severity and priority. This step is critical, as some risks may have a high likelihood with low severity while others are the opposite, making it challenging to focus on important matters first.

[**View the file report.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity)