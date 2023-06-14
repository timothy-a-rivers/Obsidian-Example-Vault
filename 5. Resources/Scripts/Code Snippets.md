---
banner: "http://4.bp.blogspot.com/-Dc0AqiN86JE/UKd40WwEvaI/AAAAAAAABEY/D1pS-tZPUNY/s1600/earth-fantasy-3d-HD_wallpapers.jpg"
banner_lock: true
banner_icon: ⌨
note_type: resource
banner_y: 0.348
---
# Code Snippets
### Helpful code snippets to keep track of and use later

## Get a list of all column headers from a given table
```sql
SELECT
	name
FROM 
	sys.columns 
WHERE 
	OBJECT_ID = OBJECT_ID('[TABLE NAME]')
```

## Search for a particular column
```sql
SELECT 
	*
FROM
	INFORMATION_SCHEMA.COLUMNS
WHERE
	COLUMN_NAME LIKE '%orig%'
```

## Get the minimum value of a particular metric compared to other metrics
```sql
SELECT MIN(f) FROM (VALUES (metric 1),(metric 2), (etc...)) AS Fields(f)) AS MinF
```

