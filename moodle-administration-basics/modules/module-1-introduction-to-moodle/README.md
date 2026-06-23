# Module 1: Introduction to Moodle

**Time:** 9:00 AM – 9:30 AM  
**Duration:** 30 minutes  
**Delivery style:** Presentation with short demo

### What You Will Be Able to Do

By the end of this module, you should be able to:

- Explain what Moodle is and why organizations use it.
- Describe the concept of a Learning Management System.
- Identify common Moodle use cases in universities.
- Recognize the main parts of Moodle at a high level.
- Understand how users interact with Moodle from different roles.


## Topic Files

- [What Is Moodle?](01-what-is-moodle.md)
- [LMS Concept](02-lms-concept.md)
- [Moodle Ecosystem](03-moodle-ecosystem.md)
- [Common Use Cases in Universities](04-common-use-cases-in-universities.md)
- [High-Level Architecture](05-high-level-architecture.md)


### Hands-On Notes for You

- Keep this module conceptual and visual.
- Use a simple architecture diagram on a slide or whiteboard.
- Avoid discussing PHP internals or database schema details.
- List the systems your organization currently integrates with.
- Emphasize that Moodle administrators need both application awareness and basic infrastructure awareness.

### Real-World Examples

- A student logs in and downloads lecture notes. Moodle checks the student’s account, course enrolment, permissions, and file access before serving the file.
- A teacher uploads a PDF. Moodle stores file information in the database and stores the actual file in the Moodle file storage system under `moodledata`.
- A scheduled course announcement is posted. Cron may be responsible for sending notification emails later.

### Demo Ideas

- Show the Moodle front page.
- Log in as an administrator and show the dashboard.
- Open a sample course and show course sections, activities, participants, and grades.
- Briefly show the Site administration menu without changing settings.

### Key Takeaway Summary

- Moodle is an LMS used to manage online learning.
- Moodle supports many user roles, including students, teachers, administrators, and support staff.
- Moodle depends on application files, a database, `moodledata`, cron, and server infrastructure.
- Technical staff should understand Moodle as both a learning platform and a web application.

---
