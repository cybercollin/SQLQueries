<h1>Database SQL queries to investigate Cybersecurity Incidents</h1>

<h2>Description</h2>
This lab simulated working for an organization that has requested assitance to improving their security posture through investigation of security issues and scheduling updates as needed. My initial task is to gather information from our database to present data-based decisions to our security manager. I will directly query the database and use a variety of filters to obtain this data.  


<br />

<h2>Languages and Utilities Used</h2>

- <b>SQL</b> 

<h2>Environments Used </h2>

- <b>Coursera Lab Environment</b> 

<h2>Project walk-through:</h2>

<p>
Our normal business hours end at 18:00, Monday through Friday. Management informed me that there was a possible incident that occurred after business hours. I will proceed to check out failed login attempts after business hours.
<br />
<br />
<img src="https://i.imgur.com/bZ9mMzh.png" height="80%" width="80%" alt="SQL Queries"/>
<br />
<br />
We have a log_in_attempts table which stores data about who, when, where and how (success/failure) our staff access the system. I issued a query which said: “Show me everything from our login attempts data that occurred after 18:00 and was also a login failure”.  In SQL this translates as <b>SELECT * FROM log_in_attempts WHERE login_time > ‘18:00’ AND success =0;</b>. This query returned a total of 19 entries that satisfied this question. Proving that there were multiple failed access attempts after hours.  
<br />
<br />
<hr>
Management informed our cybersecurity team that a suspicious event occurred on 2022-05-09 and they want all login activity from this day and the day previous to be retrieved.
<br />
<br />
<img src="https://i.imgur.com/vClwpMG.png" height="80%" width="80%" alt="SQL Queries"/>
For demonstration purposes I left out the middle of the query and showed only the beginning and end.
<br />
<br />
<img src="https://i.imgur.com/7Np79JQ.png" height="80%" width="80%" alt="SQL Queries"/>
<br />
<br />
Within our log_in_attempts table we store the dates of attempts. I issued a query asking: “Show me all of the login attempts that occurred on 2022-05-08 or 2022-05-09” by using the SQL statement <b></b>SELECT * FROM log_in_attempts WHERE login_date = ‘2022-05-08’ OR
login_date = ‘2022-05-09’;</b>. This question to the database returned 75 successful results.
<br />
<br />
<hr>
Management has explained that they suspect the issue is occuring with login attempts happening outside of Mexico (where login attemps should only be coming from Mexico). I investigated the issue further by filtering the results on the MEX and MEXICO country codes within the database entries:
<br />
<br />
<img src="https://i.imgur.com/F2dxKhF.png" height="80%" width="80%" alt="SQL Queries"/>
<img src="https://i.imgur.com/Gfi4gJ5.png" height="80%" width="80%" alt="SQL Queries"/>






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
