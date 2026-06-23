# Module 1: Advanced Platform Architecture

## Purpose

Help participants understand how Moodle components are arranged in production and how architecture choices affect reliability, maintainability, and performance.

## Learning Objectives

- Compare single-server, split-tier, and horizontally scaled Moodle deployments.
- Explain how application files, database, `moodledata`, cache, sessions, and cron interact.
- Identify risks in environment separation, shared storage, and background processing.

## Key Topics

- Production topology and environment separation.
- Web server, PHP runtime, database, cache, and file-storage responsibilities.
- Load balancing and session considerations.
- Cron, scheduled tasks, and ad-hoc tasks in production.
- Configuration management and documentation expectations.

## Trainer Notes

Use diagrams to show request flow from browser to Moodle, database, cache, and file storage. Emphasize that architecture decisions should match user volume, assessment schedules, recovery targets, and team capability.
