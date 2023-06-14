---
banner: "https://www.pixelstalk.net/wp-content/uploads/images7/Fantasy-Landscape-Wallpaper-Desktop.jpg"
banner_icon: 🔴
banner_y: 0.932
banner_lock: true
note_type: periodic/daily
full-date: <% tp.file.title %>
day: <% tp.date.now("dddd", 0, tp.file.title, "YYYY-MM-DD") %>
week: <% tp.date.now("YYYY-[W]ww", 0, tp.file.title, "YYYY-MM-DD") %>
month: <% tp.date.now("MMMM", 0, tp.file.title, "YYYY-MM-DD") %>
year: <% tp.date.now("YYYY", 0, tp.file.title, "YYYY-MM-DD") %>
fileClass: Daily
IT_Mod: 
Mod_Summary: 
summary:
---
----
⠀
## [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|↶ YESTERDAY]] ⁝ [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|TOMORROW ↷]]
# ◌ <% tp.date.now("dddd -  MMMM Do YYYY", 0, tp.file.title, "(📅) YYYY-MM-DD") %>

#### ✓  TASKS

######  ↑ TOP TASK
----
```ad-attention
title: Top Tasks
```tasks
due before <% tp.date.now("YYYY-MM-DD",2, tp.file.title, "YYYY-MM-DD") %>
not done
priority is high
short mode
hide task count
status.type is not NON_TASK
```

###### ○ TASKS
---
```ad-todo
title: Tasks
icon: tasks
```tasks
not done
priority is below high
short mode
hide task count
status.type is not NON_TASK
```

###### ✓ COMPLETED TODAY
----
```ad-done
title: Completed Today

```tasks
done date is <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
hide task count
status.type is not NON_TASK
```

#### ↻ DAILIES

###### ◧ MEETINGS
----

```dataview
TABLE WITHOUT ID
file.link AS "Meeting",
time as "Time",
purpose AS "Summary"
FROM "4. Areas/Meeting Notes"
WHERE file.name != "Meeting Notes"
WHERE date = date(<% tp.file.title %>)
SORT time DESC
```

###### DAILY NOTES
----
* 


## Created Today

```dataview
TABLE dateformat(file.ctime, "MMMM dd, yyyy") AS Created, dateformat(file.mtime, "MMMM dd, yyyy - HH:mm") AS "Last modified"
WHERE file.cday = this.file.day
WHERE file.name != this.file.name
SORT file.mtime desc
LIMIT 10
```

## Last Modified Today

```dataview

TABLE dateformat(file.ctime, "MMMM dd, yyyy") AS Created, dateformat(file.mtime, "MMMM dd, yyyy - HH:mm") AS "Last modified"
WHERE file.mday = this.file.day
WHERE file.name != this.file.name
SORT file.mtime desc
LIMIT 10

```
