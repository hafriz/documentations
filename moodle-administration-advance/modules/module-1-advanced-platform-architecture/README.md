# Module 1: Advanced Platform Architecture

## Why This Module Matters to You

This module helps you understand how Moodle components are arranged in production and how architecture choices affect reliability, maintainability, and performance.

## What You Will Be Able to Do

- Compare single-server, split-tier, and horizontally scaled Moodle deployments.
- Explain how application files, database, `moodledata`, cache, sessions, and cron interact.
- Identify risks in environment separation, shared storage, and background processing.

## Topics You Will Practice

- Production topology and environment separation.
- Web server, PHP runtime, database, cache, and file-storage responsibilities.
- Load balancing and session considerations.
- Cron, scheduled tasks, and ad-hoc tasks in production.
- Configuration management and documentation expectations.

## Hands-On Notes for You

Use diagrams in your notes to trace request flow from browser to Moodle, database, cache, and file storage. Emphasize that architecture decisions should match user volume, assessment schedules, recovery targets, and team capability.
