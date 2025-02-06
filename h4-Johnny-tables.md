# H4 Homework

## X) Summaries

### <ins>OWASP 10 (2021)</ins>  


<ins>A01:2021 - Broken Access Control</ins>    
- Broken/ faulty access control is ranked 1st in the 2021 list of top 10 web application security risk. It’s a major security risk found in 94% of evaluated web applications.
- Broken access control refers situations where users gain access data and/or can perform actions beyond their intended permissions. Access control should be enforced to restrict user actions to their permitted access levels. 
- Some common vulnerabilities:
  - Principle of least privilege or deny by default -rule is not enforced. Users indiscriminately gain access to more capabilities than needed. 
  - Escalating privileges by tampering with tokens (e.g. JWTs, access control tokens), cookies or hidden fields to access functions meant for high-level users, such as admins.
  - Bypassing restrictions/control checks by modifying either URLs, API requests or the application’s internal state.
  - CORS (Cross-Origin Resource Sharing) misconfiguration. Allows access from unauthorized or untrusted origins/domains.
- Prevention
  - Implement access control methods on the server-side (or server-less API). Unlike on the client-side, attackers cannot interfere with access control checks or metadata there.
  - Deny access by default
  - Centralize access control and apply it consistently throughout the application
  - Monitor, log and limit access attempts. Alert admins for suspicious patterns, such as repeated failures.
  - Invalidate session tokens after logout.


### <ins>References</ins> 
- A01:2021 - Broken Access Control at https://owasp.org/Top10/A01_2021-Broken_Access_Control/ 
- A05:2021 - Security Misconfiguration at https://owasp.org/Top10/A05_2021-Security_Misconfiguration/ 
- A06:2021 - Vulnerable and Outdated Components at https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/ 
- A03:2021 – Injection at https://owasp.org/Top10/A03_2021-Injection/ 


### <ins>Web comic: Exploits of a mom</ins>  

- Description
  - The web comic describes a situation where a user input is structured as a SQL injection/ malicious SQL command (`Robert '); DROP TABLE Students; --”`). The software system in question didn’t properly handle (escape) special characters in the input, which lead to major data loss. 

- Lesson:
  - Sanitize and validate user inputs to prevent SQL injection vulnerabilities


### <ins>References</ins>  
- Munroe: xkcd 327: Exploits of a Mom at https://xkcd.com/327/ 


## X) Summaries
### <ins>References</ins>  
