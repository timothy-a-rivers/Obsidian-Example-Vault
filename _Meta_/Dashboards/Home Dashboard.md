---
banner: "https://www.goodfreephotos.com/albums/other-landscapes/sunlight-and-road-through-the-forest.jpg"
banner_icon: 🧭
banner_lock: true
banner_y: 0.92168
---

```ad-note
title: Start Here!
icon: paw
color: 109, 72, 8

[[Getting Started]]

```



```ad-warning
title: Daily Motivation
icon: infinity
color:  134, 110, 165
***Everything will be all right in the end. If it's not all right, it's not the end.***
```
# Dashboard

> [!multi-column]
>
>> [!agenda] Agenda
>>📆 `$= '[['+moment().format("YYYY-MM-DD")+'|Today]]'`  
>>🗓 `$= '[['+moment().format("YYYY-[W]ww")+'|Week]]'`  
>>📅 `$= '[['+moment().format("YYYY - MM-MMM")+'|Month]]'`
>
>> [!project] Work
>> 🏗️ [[3. Projects|Projects]]
>> 📐 [[Obsidian Vault Example]]
>
>> [!vault] Explore
>> 👥 [[Meeting Notes]]
>> 📧 [[Email Notes]]
>> 📎 [[Attachments]]
>> 📇 [[Contacts]]
>> ⌨ [[Code Snippets]]

---
## ✅ Tasks
[[2. Tasks|Tasks Dashboard]] | [[Task Inbox]] | [[Completed|Completed Tasks]]

````ad-warning
title: Urgent Tasks
```tasks
not done
priority is high
hide task count
short mode
```
````

````ad-success
title: Tasks
icon: fa-check-square
```tasks
not done
hide task count
priority is below high
short mode
status.type is not NON_TASK
```
````

---
## 👥 Upcoming Meetings
```dataview  
TABLE WITHOUT ID
file.link AS "Meeting (Within 3 Days)",
date AS "Date",
time AS "Time",
purpose AS "Summary"
FROM "4. Areas/Meeting Notes"
WHERE file.name != "Meeting Notes"
WHERE date >= date(today) AND date <= date(today)+dur(3days)
SORT date ASC, time ASC
LIMIT 10
```

## 👥 Recent Meetings
```dataview  
TABLE WITHOUT ID
file.link AS "Meeting (Within 3 Days)",
date AS "Date",
time AS "Time",
purpose AS "Summary"
FROM "4. Areas/Meeting Notes"
WHERE file.name != "Meeting Notes"
WHERE date < date(today) AND date >= date(today) - dur(3days)
SORT date ASC, time ASC
LIMIT 10
```

---
## 🕓 Recent Files
```dataview  
table file.ctime as Created, file.mtime as "Last modified"  
where file.name != this.file.name   
sort file.mtime DESC  
limit 10  
```

---
## 📒 Fleeting Notes

