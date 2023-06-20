---
banner: "![[Sunset_Mountain.jpg]]"
banner_icon: 🟢
banner_lock: true
banner_y: 0.708
note_type: periodic/weekly
week_end: <% tp.date.now("YYYY-MM-DD", 5, tp.file.title, "gggg-[W]ww") %>
week: <% tp.date.now("ww", 0, tp.file.title, "gggg-[W]ww") %>
month: <% tp.date.now("MMMM", 0, tp.file.title, "YYYY--WW") %>
year: <% tp.date.now("YYYY", 0, tp.file.title, "gggg-[W]ww") %>
---

# Weekly Overview

## Days:
```dataview
TABLE WITHOUT ID
file.link AS "Date", day AS "Day of the Week", summary AS "Summary"
FROM "5. Resources/Journal/Daily Notes"
WHERE week = "<% tp.file.title %>"
SORT file.name ASC
```

````ad-success
title: Tasks Completed
```tasks
done after <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>
done before <% tp.date.now("YYYY-MM-DD", 6, tp.file.title, "gggg-[W]ww") %>
short mode
hide task count
hide backlinks
```
````

## IT Modernization Work:
```dataviewjs

const query = `TABLE WITHOUT ID day AS "Day", IT_Mod AS "Modernization Hours", Mod_Summary AS "Summary"
FROM "5. Resources/Journal/Daily Notes"
WHERE week = "<% tp.file.title %>"
SORT file.name ASC`

const TotalRow = "Total:";

let DQL = await dv.tryQuery(query);
const sums = [TotalRow];
for (let i = 1; i < DQL.headers.length; i++) {
    let sum = 0;
    const dataType = getDatatypeOfColumn(i, DQL.values)
    if (!["number", "duration"].includes(dataType)) {
        sums.push("")
        continue;
    }
    for (let k = 0; k < DQL.values.length; k++) {
        let currentValue = DQL.values[k][i];
        if (currentValue) sum += currentValue 
    }
    if (!sum) sum = ""
    sums.push(dataType === "duration" ? luxon.Duration.fromMillis(sum) : sum);
}

function getDatatypeOfColumn(columnNo, values) {
    let i = 0;
    let datatype;
    while (i < DQL.values[0].length && (!datatype || datatype === "null")) {
        datatype = dv.func.typeof(DQL.values[i][columnNo])
        i++;
    }
    return datatype;
}

let hrArray = Array(DQL.headers.length).fill('<hr style="padding:0; margin:0 -10px;">');
DQL.values.push(hrArray)
DQL.values.push(sums)

dv.table(DQL.headers, DQL.values)

```
```ad-warning
title: 
```
## Daily Meetings:
---
### Monday Meetings:
```dataview
TABLE WITHOUT ID
file.link AS "Meeting", date as "Date", time AS "Time", project AS "Project", purpose as "Summary"
FROM "4. Areas/Meeting Notes"
WHERE date = date("<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "gggg-[W]ww") %>")
```

### Tuesday Meetings:
```dataview
TABLE WITHOUT ID
file.link AS "Meeting", date as "Date", time AS "Time", project AS "Project", purpose as "Summary"
FROM "4. Areas/Meeting Notes"
WHERE date = date("<% tp.date.now("YYYY-MM-DD", 2, tp.file.title, "gggg-[W]ww") %>")
```

### Wednesday Meetings:
```dataview
TABLE WITHOUT ID
file.link AS "Meeting", date as "Date", time AS "Time", project AS "Project", purpose as "Summary"
FROM "4. Areas/Meeting Notes"
WHERE date = date("<% tp.date.now("YYYY-MM-DD", 3, tp.file.title, "gggg-[W]ww") %>")
```

### Thursday Meetings:
```dataview
TABLE WITHOUT ID
file.link AS "Meeting", date as "Date", time AS "Time", project AS "Project", purpose as "Summary"
FROM "4. Areas/Meeting Notes"
WHERE date = date("<% tp.date.now("YYYY-MM-DD", 4, tp.file.title, "gggg-[W]ww") %>")
```

### Friday Meetings:
```dataview
TABLE WITHOUT ID
file.link AS "Meeting", date as "Date", time AS "Time", project AS "Project", purpose as "Summary"
FROM "4. Areas/Meeting Notes"
WHERE date = date("<% tp.date.now("YYYY-MM-DD", 5, tp.file.title, "gggg-[W]ww") %>")
```
