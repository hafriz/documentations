# Exercises / Discussion Questions

Use these trainee activities during hands-on practice. Complete them individually, in pairs, or as small-group discussions, and keep your answers as reference notes after training.

## Exercise 1: Identify the Component

**Instructions:** Match each issue with the most likely Moodle component.

| Issue | Component Options |
|---|---|
| Forum emails are not being sent | Cron, email service, scheduled tasks |
| Users cannot log in using institutional accounts | Authentication, SSO, LDAP |
| File uploads fail with a storage error | `moodledata`, disk space, permissions |
| All pages show a database connection error | Database, `config.php`, network |
| Theme changes do not appear immediately | Cache, theme settings |

Discussion questions:

- Which issues can a Moodle administrator check first?
- Which issues require server or database administrator support?

## Exercise 2: Authentication vs Enrolment

**Scenario:** A student can log in to Moodle but cannot access Biology 101.

Questions:

1. Is this primarily an authentication issue or an enrolment issue?
2. What should you check first?
3. What course settings might affect visibility?
4. What role should the student normally have in the course?

Expected discussion:

- The student can log in, so authentication is probably working.
- Check course enrolment, course visibility, role assignment, and restrictions.

## Exercise 3: Role Assignment Discussion

**Scenario:** A department assistant needs to help manage courses for the Faculty of Engineering but should not administer the entire Moodle site.

Questions:

1. Should this person be made a site administrator?
2. What role or context might be more appropriate?
3. Why is least privilege important?

Expected discussion:

- Avoid unnecessary site administrator access.
- Consider manager permissions at the category level.
- Assign only the permissions needed for the task.

## Exercise 4: Performance Brainstorm

**Scenario:** Moodle becomes slow every Monday at 9:00 AM.

Questions:

1. What information would you collect?
2. What server resources might be involved?
3. Could scheduled tasks be related?
4. Could user behavior or timetable patterns be related?
5. What recent changes should be reviewed?

Expected discussion:

- Investigate usage patterns, server metrics, database load, cron timing, backups, and recent changes.

## Exercise 5: Plugin Evaluation

**Scenario:** A lecturer requests installation of a plugin for a new interactive activity.

Questions:

1. What should you check before installing the plugin?
2. Should it be installed directly in production?
3. Who should approve the change?
4. What support risks should be considered?

Expected discussion:

- Check compatibility, maintenance status, documentation, privacy, performance, and staging test results.

## Exercise 6: Maintenance Planning

**Instructions:** In small groups, create a simple weekly Moodle maintenance checklist for your organization.

Include:

- Availability checks.
- Cron checks.
- Backup checks.
- Disk space checks.
- Plugin update review.
- Support ticket trend review.
- Security or administrator access review.

Group sharing:

- Each group presents three checklist items they believe are most important.

---
