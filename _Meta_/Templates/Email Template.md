---
banner: "https://i.redd.it/ue05165ttiz31.png"
banner_y: 0.744
banner_icon: ✉️
banner_lock: true
fileClass: Email
project:
date:
sender: {{VALUE:Email Sender}}
purpose: {{VALUE:Email Subject}}
---
<% await tp.file.move("/4. Areas/Email Notes/" + tp.file.title) %>
**Project:** `= this.project`
**Email Date:** `= this.email_date`
**Sender:** [[{{VALUE:Email Sender}}]]
# {{VALUE:Email Subject}}

## 👥 Recipients
---
| Name               | Department/Team                     | Title           |
| ------------------ | ----------------------------------- | --------------- |


## 📧 Intial Email
---



## ✅ Tasks
---


## 📩 Previous Emails
---
