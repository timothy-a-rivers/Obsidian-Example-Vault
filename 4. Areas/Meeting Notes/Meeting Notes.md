---
banner: "https://www.pixelstalk.net/wp-content/uploads/2016/11/Fantasy-Landscape-Desktop-Pics-Wallpapers.jpg"
banner_y: 0.616
---

# Meetings Overview

```dataview

TABLE time AS "Time", file.mtime as "Last Modified", project AS "Project", purpose AS "Summary"
FROM "4. Areas/Meeting Notes"
WHERE file.name != "Meeting Notes"
SORT file.mtime DESC

```

