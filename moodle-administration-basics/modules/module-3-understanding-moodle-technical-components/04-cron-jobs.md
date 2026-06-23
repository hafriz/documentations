# Cron Jobs


Cron is a scheduler that runs background tasks automatically. In Moodle, cron is essential.

Moodle cron handles tasks such as:

- Sending forum notifications.
- Processing scheduled tasks.
- Running cleanup operations.
- Updating completion records.
- Processing analytics tasks.
- Sending assignment notifications.
- Running automated backups if configured.
- Synchronizing some enrolments or external data.

A typical Moodle cron command may look like this:

```bash
php /path/to/moodle/admin/cli/cron.php
```

The exact command and schedule depend on the server environment.

Trainee note: If cron is not running, Moodle may appear to work at first, but background features will slowly fail or become delayed. Notifications may not send, scheduled tasks may remain pending, and cleanup may not happen.
