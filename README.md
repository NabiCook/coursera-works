# Coursera: Google Cybersecurity Professional Certificate

This repository contains my portfolio activities and assignments from the Google Cybersecurity on Coursera. The work below demonstrates my work in Python automation, Linux/SQL, network security, and security data analysis.

---

## Featured Projects & Skills

### Automating Cybersecurity Tasks with Python

* **Example: Algorithm for file updates**
    This opens and makes changes to the file.

    ```python
import_file = "allow_list.txt"
with open(import_file, "r") as file:
	ip_addressess = file.read()
    ```
this code snippet keeps the file opnend as "r" read mode to access the contents inside.

once the file was loaded by .read(), the contents are in string format.
To convert strings of IP addresses into lists, we need to use .split()

```python
ip_address.split()```

then for loop is ued to loop through every elements within the list ip_addressess, 
looking for a match in remove_list.
once finding a match, .remove() deletes the following entry from the list.

```python
for element in ip_addresses:
    if element in remove_list:
        ip_addresses.remove(element)

ip_addresses = " ".join(ip_addresses)   
```
" " was used to give space in between and .join() to put everything back to the string, reformatting the data for a later file save.

```python
  with open(import_file, "w") as file:
    file.write(ip_addresses)
```
This time, file is opened in "w" write mode and .write() was used to store the string data back to the file.

[**Browse the file here.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity/Automating-Cybersecurity-Tasks-with-Python)

---

### Linux and SQL for Cybersecurity

This section showcases the use of essential Linux command-line tools and SQL queries for log analysis, file system auditing, and database inspection.

* **Example: Linux Permission Command**
    chmod allows to makes changes to the permission to prevent unauthorized access to the files.  Linux shows permissions in User, Group, and Other order, with each having read, write, execute permissions. For instance, project_k.txt has a permission of -rw-rw-rw-, which states user, group, and other has read and write permissions of the file.
```bash
chmod o-w project_k.txt
```
the command above uses "-" to remove the "w" write permission from Other group, making it read-only 
[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/File%20permissions%20in%20Linux.docx)


* **Example: SQL Query**
    Querying a database to identify all employees in the 'Sales' department who have administrative access.
    ```sql
    SELECT *
    FROM log_in_attempts
    WHERE login_time > '18:00' AND success =0;
    ```
This quesry looks for any failed (0 = fail, 1 = success) login attempts made outside of work hours, after 6 PM in particular. This step is critical in cyber security to identify suspecious behaviors.

[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/Apply%20filters%20to%20SQL%20queries.docx)

---


### Incident Report Analysis

This hands-on activity focused on examining log data generated from tools like tcpdump or wireshark and detect suspecious network activities / attacks. In this case, multiple ICMP packets were identified, indicating an ICMP flood attack or (D)DoS. The report contains several suggestions to mitigate the risk, such as configuring firewall rules, blocking unused ports, black-listing IP addressed used for attacks, and installing IDPS.

[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/Incident%20report%20analysis.docx)


This report was on an incident where a sales manager left the internal-only files access available, resulting in a leak prior to the release. After a through analysis of the situation, suggestions were made to meet the NIST SP 800-53. For this case, a user access timeout for the file system, and a user based permission control must be implemented to prevent third party vendors from accessing the mis-sent files.
If there was an automatic timeout system, the business partner wouldn't have had access to the link since the access was already revoked by the time they received the wrong link, If the permission system limited what the users could view based on their account privileges, this incident could have been avoided since the business partner does not have permissions to view  internal-only content.

[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/Activity%20Template_%20Data%20leak%20worksheet.docx)


---

### Risk and Compliance Analysis
This activity simulates hands-on experience of a security compliance audit. Various criteria were evaluated according to relavant guidelines, such as PCI DSS for payment security and GDPR for EU compliance.

[**View the file report.**](https://github.com/NabiCook/coursera-works/blob/main/GoogleCybersecurity/Controls%20and%20compliance%20checklist.pdf)

This activity scored each risks and ranked them in order according to their severity and priority of mitigation. This step is critical as some risks may have high likelihood with low severity while some are the opposite, making it challenging to focus on the important matter first.

[**View the file report.**](https://github.com/NabiCook/coursera-works/tree/main/GoogleCybersecurity)