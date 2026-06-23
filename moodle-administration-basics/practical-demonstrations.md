# Practical Demonstrations

Use the following demonstrations as trainee notes during the one-day introductory training. Follow along in a safe demo Moodle site, not a live production site.

## Demo 1: Moodle User Experience Overview

**Purpose:** Help you see Moodle from the perspective of different user roles.

Steps:

1. Open the Moodle front page.
2. Log in as a student.
3. Open a course.
4. View resources, activities, grades, and participant list if allowed.
5. Log out and log in as a teacher.
6. Turn editing on and show course editing controls.
7. Log in as an administrator and show Site administration.

Discussion points:

- Different roles see different options.
- Access depends on permissions and enrolment.
- Support staff must often ask which role the user has.

## Demo 2: Site Administration Navigation

**Purpose:** Help you become familiar with the administration interface.

Steps:

1. Open Site administration.
2. Browse the major administration categories.
3. Use the administration search box.
4. Open Users, Courses, Plugins, Appearance, Server, and Reports sections.
5. Explain that not every setting should be changed without planning.

Discussion points:

- The search box is useful for finding settings quickly.
- Some settings are site-wide and high impact.
- Documentation and change control are important.

## Demo 3: Create and Manage a User

**Purpose:** Practice the basic flow of manual user administration.

Steps:

1. Create a test user.
2. Set required profile fields.
3. Confirm authentication method.
4. Search for the user.
5. Edit the profile.
6. Suspend and unsuspend the account if appropriate.

Discussion points:

- Manual accounts are useful for testing and special cases.
- Production accounts may come from SSO or directory services.
- Suspending is often safer than deleting immediately.

## Demo 4: Course Creation and Enrolment

**Purpose:** Practice the basic course setup sequence.

Steps:

1. Create a course category.
2. Create a course.
3. Set course full name, short name, category, visibility, and format.
4. Enrol a teacher.
5. Enrol a student.
6. Confirm what each user can see.

Discussion points:

- Course visibility affects student access.
- Enrolment controls who can enter the course.
- Role assignment controls what users can do.

## Demo 5: Add a Resource and Activity

**Purpose:** Practice identifying the difference between resources and activities.

Steps:

1. Open a demo course as a teacher.
2. Turn editing on.
3. Add a File resource.
4. Add a Forum activity.
5. Add an Assignment activity if time allows.
6. View the course as a student.

Discussion points:

- Resources are often content delivery tools.
- Activities involve interaction or assessment.
- Support teams should understand common activity settings.

## Demo 6: Technical Components Walkthrough

**Purpose:** Connect the Moodle interface you use to the backend components that support it.

Steps:

1. Show the Moodle application directory in a training server.
2. Identify `config.php` without exposing sensitive credentials.
3. Show the configured `moodledata` path.
4. Show a database connection setting conceptually.
5. Show the Scheduled tasks page.
6. Run cron manually if safe.

Discussion points:

- Moodle is more than a website.
- Database and `moodledata` are essential for backup and recovery.
- Cron must run regularly.

## Demo 7: Cache and Theme Change

**Purpose:** Show a safe customization example.

Steps:

1. Open theme settings.
2. Change a simple branding option in a demo environment.
3. Purge caches if needed.
4. Refresh the front page.
5. Discuss testing on mobile and different browsers.

Discussion points:

- Theme changes affect user experience.
- Cache can delay visible changes.
- Branding should be tested carefully.

## Demo 8: Troubleshooting Course Access

**Purpose:** Demonstrate structured troubleshooting.

Scenario: A student says they cannot access a course.

Steps:

1. Confirm the student account exists.
2. Confirm the student can log in.
3. Check whether the course is visible.
4. Check whether the student is enrolled.
5. Check role assignment.
6. Check availability restrictions if present.
7. Document the result.

Discussion points:

- Access problems often involve multiple layers.
- Authentication and enrolment are different.
- Course visibility is a common cause of access issues.

---
