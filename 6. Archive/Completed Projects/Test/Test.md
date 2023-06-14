---
banner: "https://i.redd.it/ckdws8pnsy291.jpg"
tags: project
banner_y: 0.844
banner_icon: 💥
project_page_type: project
target: 
goal: Test
due: 10/01/2023
complete: ❌
---
[[3. Projects|Back to dashboard]]
# Test
 
> [!multi-column]
>
>> [!blank|wide-2]
>> ## 📐 Project Info
>> ---
>> Started:: June 13, 2023
>> Deadline:: 10/01/2023
>> Description:: Test
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
>> WHERE contains(project,  "Test")
>> ```
>
>> [!success|wide-5] Completed
>> ```dataview
>> TASK
>> WHERE completed
>> WHERE contains(project,  "Test")
>> ```
>

> [!multi-column]
>
>> [!question] Questions
>> ```dataview
>> TASK
>> WHERE contains(project,  "Test")
>> WHERE status = "?"
>> ```
>
>> [!error] Fixes
>> ```dataview
>> TASK
>> WHERE contains(project,  "Test")
>> WHERE status = "f"
>> ```

>[!example] Files
>> ```dataview  
>> TABLE   
>> FROM "3. Projects/Test"
>> WHERE file.name != "Test"
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
>> WHERE contains(project, "Test")
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
>> WHERE contains(project,  "Test")
>> ```

## 📒 Notes
---
* 

## 📇 Contacts
---

