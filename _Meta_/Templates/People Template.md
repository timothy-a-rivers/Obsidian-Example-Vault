---
Office:
Division:
Team:
Title:
Email:
Aliases:
---
tags:: [[People MOC]]

## <% tp.file.title %>
<% await tp.file.move("/4. Areas/Contacts/" + tp.file.title) %>

## Notes:

* 

-----------------------------------------------------------------------

## Meetings:
```dataview
TABLE date as "Meeting Date", purpose AS "Summary"
FROM "4. Areas/Meeting Notes"
WHERE contains(file.outlinks, [[<% tp.file.title %>]])
SORT file.cday DESC
```

## Emails:
```dataview
TABLE date AS "Email Date", purpose AS "Summary"
FROM "4. Areas/Email Notes"
WHERE Sender = "<% tp.file.title %>"
SORT file.cday DESC
LIMIT 10
```

