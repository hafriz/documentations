# Module 3: Understanding Moodle Technical Components

**Time:** 11:00 AM – 12:00 PM  
**Duration:** 60 minutes  
**Delivery style:** Presentation and technical walkthrough

### What You Will Be Able to Do

By the end of this module, you should be able to:

- Identify the main Moodle technical components.
- Explain the purpose of the Moodle code directory.
- Explain the purpose of the database.
- Explain the purpose of `moodledata`.
- Understand why cron is required.
- Describe a basic Moodle backend workflow.


## Topic Files

- [Moodle Directory Structure](01-moodle-directory-structure.md)
- [Database Overview](02-database-overview.md)
- [`moodledata`](03-moodledata.md)
- [Cron Jobs](04-cron-jobs.md)
- [Backend Workflow](05-backend-workflow.md)


### Hands-On Notes for You

- Use a diagram showing browser, web server, Moodle code, database, `moodledata`, cron, and email service.
- Avoid detailed database schema discussion.
- Make sure you understand that backup requires more than copying Moodle code.
- Emphasize the importance of `config.php`, but do not display real credentials in a live production environment.
- If demonstrating command-line paths, use a training environment only.

### Real-World Examples

- If the database server is down, users may see a database connection error and the site may not load.
- If disk space is full in the `moodledata` partition, uploads and cache generation may fail.
- If cron has not run for days, forum notifications and scheduled tasks may be delayed.
- If the Moodle application directory is updated incorrectly, plugins or themes may break.

### Demo Ideas

- Show the Moodle application directory in a safe training environment.
- Open `config.php` and point out key settings without exposing passwords in production.
- Show the `moodledata` path from configuration.
- Show the Scheduled tasks page in Site administration.
- Run cron manually in a demo environment and review output.
- Show where Moodle displays environment or server checks.

### Key Takeaway Summary

- Moodle depends on code files, a database, `moodledata`, cron, and server services.
- The database stores structured records and settings.
- `moodledata` stores uploaded and generated files.
- Cron is required for background processing.
- A complete backup strategy must include Moodle code, database, and `moodledata`.

---
