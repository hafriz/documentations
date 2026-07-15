# Create a Hello World Moodle Block with the Plugin Skeleton Generator

## Goal

This hands-on guide shows how to create a very small Moodle block plugin named **Hello World** by using Moodle's Plugin Skeleton Generator. The final block can be added to a Moodle course page or dashboard and displays a simple greeting.

## What You Will Build

- **Plugin type:** Block
- **Plugin folder:** `blocks/helloworld`
- **Component name:** `block_helloworld`
- **Visible block title:** `Hello World`
- **Visible block content:** `Hello world from my first Moodle block!`

## Before You Start

Prepare a development Moodle site, not a production site.

You need:

1. Access to the Moodle code directory.
2. Administrator access to the Moodle site.
3. PHP command-line access.
4. Git installed on the server or local development machine.
5. Moodle developer debugging enabled during development.

> **Important:** Always test new plugins on a local or staging Moodle site before installing them on production.

## Step 1: Install the Plugin Skeleton Generator

From the root of your Moodle installation, install the skeleton generator into `admin/tool/pluginskel`.

```bash
cd /path/to/moodle
git clone https://github.com/mudrd8mz/moodle-tool_pluginskel.git admin/tool/pluginskel
php admin/cli/upgrade.php
```

After the upgrade finishes, log in as a site administrator and confirm that Moodle installed the tool successfully.

## Step 2: Create a Skeleton Recipe File

Create a recipe file outside the final block folder, for example in `/tmp/block_helloworld.yaml`.

```yaml
component: block_helloworld
name: Hello World
release: 1.0.0
requires: 2022041900
maturity: MATURITY_ALPHA
copyright: 2026 Your Name
features:
  settings: false
  instance_allow_multiple: true
  instance_config: false
  backup_moodle2: false
```

Explanation of the important fields:

| Field | Meaning |
|---|---|
| `component` | Moodle frankenstyle component name. A block plugin must start with `block_`. |
| `name` | Human-readable plugin name. |
| `requires` | Minimum Moodle version build number supported by the plugin. Adjust this to match your Moodle version. |
| `instance_allow_multiple` | Allows the same block to be added more than once on a page. |

## Step 3: Generate the Block Plugin

Run the generator from the Moodle root directory.

```bash
cd /path/to/moodle
php admin/tool/pluginskel/cli/generate.php --recipe=/tmp/block_helloworld.yaml
```

The generator creates the initial plugin files in:

```text
blocks/helloworld/
```

Typical generated files include:

```text
blocks/helloworld/
├── block_helloworld.php
├── lang/en/block_helloworld.php
├── version.php
└── README.md
```

## Step 4: Edit the Main Block Class

Open:

```text
blocks/helloworld/block_helloworld.php
```

Update the block class so it has a title and simple content.

```php
<?php
// This file is part of Moodle - http://moodle.org/

defined('MOODLE_INTERNAL') || die();

class block_helloworld extends block_base {
    public function init(): void {
        $this->title = get_string('pluginname', 'block_helloworld');
    }

    public function get_content() {
        if ($this->content !== null) {
            return $this->content;
        }

        $this->content = new stdClass();
        $this->content->text = get_string('helloworldmessage', 'block_helloworld');
        $this->content->footer = '';

        return $this->content;
    }
}
```

## Step 5: Add Language Strings

Open:

```text
blocks/helloworld/lang/en/block_helloworld.php
```

Add or confirm these strings:

```php
<?php
// This file is part of Moodle - http://moodle.org/

defined('MOODLE_INTERNAL') || die();

$string['pluginname'] = 'Hello World';
$string['helloworld:addinstance'] = 'Add a new Hello World block';
$string['helloworld:myaddinstance'] = 'Add a new Hello World block to Dashboard';
$string['helloworldmessage'] = 'Hello world from my first Moodle block!';
```

## Step 6: Check the Version File

Open:

```text
blocks/helloworld/version.php
```

Confirm that the component name is correct.

```php
$plugin->component = 'block_helloworld';
```

If you edit the plugin after installing it, increase the plugin version number before running Moodle upgrade again.

## Step 7: Install or Upgrade the Plugin

Run the Moodle upgrade script.

```bash
cd /path/to/moodle
php admin/cli/upgrade.php
```

You can also complete the installation from the browser by logging in as administrator and visiting:

```text
Site administration > Notifications
```

## Step 8: Add the Block to a Page

1. Log in to Moodle as an administrator or teacher with editing rights.
2. Open a course page or the dashboard.
3. Turn editing mode on.
4. Open the block drawer or page block controls.
5. Select **Add a block**.
6. Choose **Hello World**.
7. Confirm that the block displays: **Hello world from my first Moodle block!**

## Step 9: Purge Caches During Development

If the title or text does not update immediately, purge Moodle caches.

```bash
cd /path/to/moodle
php admin/cli/purge_caches.php
```

Or use the Moodle interface:

```text
Site administration > Development > Purge caches
```

## Troubleshooting Checklist

| Problem | What to Check |
|---|---|
| The block does not appear in **Add a block** | Confirm the folder is `blocks/helloworld` and the component is `block_helloworld`. |
| Moodle shows a plugin validation error | Check `version.php`, class name `block_helloworld`, and language file name `block_helloworld.php`. |
| Text shows as missing string | Confirm the string key exists in `lang/en/block_helloworld.php`, then purge caches. |
| Changes do not appear | Purge caches and confirm you edited the plugin in the active Moodle code directory. |
| Installation fails | Enable developer debugging and read the exact error message from the browser or CLI output. |

## Safe Development Workflow

1. Keep the plugin in version control.
2. Make one small change at a time.
3. Run `php admin/cli/upgrade.php` after version changes.
4. Run `php admin/cli/purge_caches.php` after language, template, or display changes.
5. Test on dashboard and course pages.
6. Review Moodle coding guidelines before adding database tables, settings, forms, JavaScript, or external API calls.

## Related Documentation

- [Plugins](02-plugins.md)
- [Extending Moodle Features](05-extending-moodle-features.md)
