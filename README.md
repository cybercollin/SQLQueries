<h1>Database SQL queries to investigate Cybersecurity Incidents</h1>

<h2>Description</h2>
This lab simulated working for an organization that has requested assitance to improving their security posture through investigation of security issues and scheduling updates as needed. My initial task is to gather information from our database to present data-based decisions to our security manager. I will directly query the database and use a variety of filters to obtain this data.  


<br />

<h2>Languages and Utilities Used</h2>

- <b>SQL</b> 

<h2>Environments Used </h2>

- <b>Coursera Lab Environment</b> 

<h2>Project walk-through:</h2>

<p align="center">
Our normal business hours end at 18:00, Monday through Friday. Management informed me that there was a possible incident that occurred after business hours. I will proceed to check out failed login attempts after business hours.<br />

<img src="https://i.imgur.com/bZ9mMzh.png" height="80%" width="80%" alt="SQL Queries"/>

<br />
<br />

We have a log_in_attempts table which stores data about who, when, where and how (success/failure) our staff access the system. I issued a query which said: “Show me everything from our login attempts data that occurred after 18:00 and was also a login failure”.  In SQL this translates as <b>SELECT * FROM log_in_attempts WHERE login_time > ‘18:00’ AND success =0;</b>. This query returned a total of 19 entries that satisfied this question. Proving that there were multiple failed access attempts after hours.  

<br />
<br />
Management informed our cybersecurity team that a suspicious event occurred on 2022-05-09 and they want all login activity from this day and the day previous to be retrieved.

<img src="https://i.imgur.com/vClwpMG.png" height="80%" width="80%" alt="SQL Queries"/>


</p>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
