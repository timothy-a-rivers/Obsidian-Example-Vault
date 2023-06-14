---
banner: "https://i.redd.it/ckdws8pnsy291.jpg"
tags: project
banner_y: 0.844
banner_icon: 💥
project_page_type: project
target: 
goal: {{VALUE:Description}}
due: {{VALUE:Deadline}}
complete: ❌
---
[[3. Projects|Back to dashboard]]
# {{VALUE:Project Name}}
 
> [!multi-column]
>
>> [!blank|wide-2]
>> ## 📐 Project Info
>> ---
>> Started:: {{DATE:MMMM DD, YYYY}}
>> Deadline:: {{VALUE:Deadline}}
>> Description:: {{VALUE:Description}}
>
>> [!blank|wide-2]
>> ## 🔗 Links
>> ---
>

## 🎬 Activity
---

> [!multi-column]
> 
>> [!todo|wide-5] Tasks
>> ```dataview
>> TASK
>> WHERE status = " "
>> WHERE contains(project,  "{{VALUE:Project Name}}")
>> ```
>
>> [!success|wide-5] Completed
>> ```dataview
>> TASK
>> WHERE completed
>> WHERE contains(project,  "{{VALUE:Project Name}}")
>> ```
>

> [!multi-column]
>
>> [!question] Questions
>> ```dataview
>> TASK
>> WHERE contains(project,  "{{VALUE:Project Name}}")
>> WHERE status = "?"
>> ```
>
>> [!error] Fixes
>> ```dataview
>> TASK
>> WHERE contains(project,  "{{VALUE:Project Name}}")
>> WHERE status = "f"
>> ```

>[!example] Files
>> ```dataview  
>> TABLE   
>> FROM "3. Projects/{{VALUE:Project Name}}"
>> WHERE file.name != "{{VALUE:Project Name}}"
>> ```

## 🚀 Actions
---
* 

> [!multi-column]
>
>> [!blank|wide-3] 
>> ## 👥 Meetings
>> ---
>> ```dataview
>> TABLE WITHOUT ID
>> file.link AS "Meeting",
>> date AS "Date",
>> time AS "Time",
>> purpose AS "Summary"
>> FROM "4. Areas/Meeting Notes"
>> WHERE contains(project, "{{VALUE:Project Name}}")
>> ```
>
>> [!blank|wide-3] 
>> ## 📧 Emails
>> ---
>> ```dataview
>> TABLE WITHOUT ID
>> file.link AS "Email",
>> date AS "Date",
>> sender AS "Sender",
>> purpose AS "Summary"
>> FROM "4. Areas/Email Notes"
>> WHERE contains(project,  "{{VALUE:Project Name}}")
>> ```

## 📒 Notes
---
* 

## 📇 Contacts
---

