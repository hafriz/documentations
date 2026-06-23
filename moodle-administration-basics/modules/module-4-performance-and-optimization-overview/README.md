# Module 4: Performance and Optimization Overview

**Time:** 1:00 PM – 2:00 PM  
**Duration:** 60 minutes  
**Delivery style:** Presentation, examples, and discussion

### What You Will Be Able to Do

By the end of this module, you should be able to:

- Identify common reasons Moodle becomes slow.
- Understand basic server resource concepts.
- Explain the purpose of caching in simple terms.
- Recognize database factors that affect performance.
- List basic optimization strategies suitable for administrators.


## Topic Files

- [Why Moodle Becomes Slow](01-why-moodle-becomes-slow.md)
- [Server Resources](02-server-resources.md)
- [Cache Concepts](03-cache-concepts.md)
- [Database Considerations](04-database-considerations.md)
- [Basic Optimization Strategies](05-basic-optimization-strategies.md)


### Hands-On Notes for You

- Keep performance discussion introductory.
- Do not attempt advanced database tuning in this course.
- Use simple cause-and-effect examples.
- Explain that performance planning should consider peak events, such as online exams.
- Document normal baseline performance.

### Real-World Examples

- During final exams, 2,000 students start a quiz at the same time. The site becomes slow because the number of concurrent requests exceeds normal daily usage.
- A course page contains many large images, embedded videos, and dozens of activities. Students experience slow loading even though the server is healthy.
- Cron has not run for several days. Scheduled tasks accumulate, and when cron resumes, the server experiences a temporary spike.
- A new plugin was installed and site performance became worse. The support team reviews recent changes and plugin behavior.

### Demo Ideas

- Show Moodle performance-related administration pages, such as caching configuration and scheduled tasks.
- Demonstrate “Purge all caches” in a safe environment and explain when to use it.
- Show a sample monitoring dashboard or server resource graph.
- Show how a heavy course page differs from a well-organized course page.
- Review a sample incident timeline showing traffic spike and server response.

### Key Takeaway Summary

- Moodle performance depends on application, server, database, storage, network, plugins, and usage patterns.
- Cache helps reduce repeated work.
- Database health is critical.
- Course design can affect user experience.
- Administrators should troubleshoot performance using evidence, not guesswork.

---
