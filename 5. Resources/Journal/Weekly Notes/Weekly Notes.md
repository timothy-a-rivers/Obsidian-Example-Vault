# Weekly Notes Overview
 
```dataview
TABLE WITHOUT ID
	link(file.name) as "Day"
FROM
	"5. Resources/Journal/Weekly Notes"
SORT
	file.mtime DESC
LIMIT 10
WHERE
	file.name != "Weekly Notes"
	AND file.ctime > (date(now) - dur(7 days))
```
 
## Compled Tasks
```tasks
done date is <% tp.date.now("DD-MMM-YY", -7, tp.file.title, "YYYY-MM-DD") %>
```