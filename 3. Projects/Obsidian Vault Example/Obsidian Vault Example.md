---
banner: "https://i.redd.it/ckdws8pnsy291.jpg"
tags: project
banner_y: 0.844
banner_icon: 💥
project_page_type: project
target: 
goal: Demonstrate how I am using Obsidain for PKM
due: 
complete: ❌
---
[[3. Projects|Back to dashboard]]
# Obsidian Vault Example
 
> [!multi-column]
>
>> [!blank|wide-2]
>> ## 📐 Project Info
>> ---
>> Started:: June 12, 2023
>> Deadline:: 
>> Description:: Demonstrate how I am using Obsidain for PKM
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
>> WHERE contains(project,  "Obsidian Vault Example")
>> ```
>
>> [!success|wide-5] Completed
>> ```dataview
>> TASK
>> WHERE completed
>> WHERE contains(project,  "Obsidian Vault Example")
>> ```
>

> [!multi-column]
>
>> [!question] Questions
>> ```dataview
>> TASK
>> WHERE contains(project,  "Obsidian Vault Example")
>> WHERE status = "?"
>> ```
>
>> [!error] Fixes
>> ```dataview
>> TASK
>> WHERE contains(project,  "Obsidian Vault Example")
>> WHERE status = "f"
>> ```

>[!example] Files
>> ```dataview  
>> TABLE   
>> FROM "3. Projects/Obsidian Vault Example"
>> WHERE file.name != "Obsidian Vault Example"
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
>> WHERE contains(project, "Obsidian Vault Example")
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
>> WHERE contains(project,  "Obsidian Vault Example")
>> ```

## 📒 Notes
---
* 

## 📇 Contacts
---

