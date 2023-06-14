---
banner: "![[Sunset_Mountain.jpg]]"
banner_y: 0.58
---
# Daily Overview

```dataview
TABLE WITHOUT ID
	link(file.name) as "Day"
FROM
	"5. Resources/Journal/Daily Notes"
SORT
	file.name DESC
LIMIT 30
WHERE
	file.name != "Daily Notes"
```