# CLI Commands

| Command              | Description                   |
| -------------------- | ----------------------------- |
| `ansible`            | Run ad hoc commands           |
| `ansible-playbook`   | Execute playbooks             |
| `ansible-config`     | View and manage configuration |
| `ansible-console`    | Interactive Ansible shell     |
| `ansible-doc`        | Display module documentation  |
| `ansible-galaxy`     | Manage roles and collections  |
| `ansible-inventory`  | Display inventory information |
| `ansible-pull`       | Pull playbooks from Git       |
| `ansible-vault`      | Encrypt and decrypt files     |
| `ansible-test`       | Run Ansible tests             |
| `ansible-connection` | Internal connection utility   |

---

# Playbook Keywords

| Keyword               | Description               |
| --------------------- | ------------------------- |
| `hosts`               | Target hosts              |
| `tasks`               | Task list                 |
| `roles`               | Include roles             |
| `handlers`            | Event handlers            |
| `vars`                | Define variables          |
| `vars_files`          | Load variable files       |
| `vars_prompt`         | Prompt for variables      |
| `environment`         | Set environment variables |
| `gather_facts`        | Collect system facts      |
| `become`              | Privilege escalation      |
| `become_user`         | Target user               |
| `become_method`       | Escalation method         |
| `connection`          | Connection type           |
| `strategy`            | Execution strategy        |
| `serial`              | Rolling updates           |
| `max_fail_percentage` | Failure threshold         |
| `order`               | Host execution order      |
| `collections`         | Collections to load       |
| `module_defaults`     | Default module arguments  |
| `pre_tasks`           | Tasks before roles        |
| `post_tasks`          | Tasks after roles         |
| `force_handlers`      | Always execute handlers   |
| `any_errors_fatal`    | Stop on any error         |
| `ignore_unreachable`  | Ignore unreachable hosts  |
| `check_mode`          | Dry run                   |
| `diff`                | Show file differences     |
| `name`                | Play description          |

---

# Task Keywords

| Keyword          | Description              |
| ---------------- | ------------------------ |
| `name`           | Task description         |
| `action`         | Module to execute        |
| `args`           | Module arguments         |
| `register`       | Save module output       |
| `when`           | Conditional execution    |
| `loop`           | Iterate items            |
| `until`          | Retry until condition    |
| `retries`        | Retry count              |
| `delay`          | Delay between retries    |
| `notify`         | Trigger handler          |
| `delegate_to`    | Run on another host      |
| `delegate_facts` | Store delegated facts    |
| `ignore_errors`  | Continue after failure   |
| `failed_when`    | Custom failure condition |
| `changed_when`   | Custom changed condition |
| `run_once`       | Execute once             |
| `throttle`       | Limit parallel execution |
| `async`          | Background execution     |
| `poll`           | Async polling            |
| `timeout`        | Execution timeout        |
| `become`         | Elevate privileges       |
| `environment`    | Environment variables    |
| `tags`           | Task tags                |
| `check_mode`     | Override check mode      |
| `diff`           | Override diff mode       |

---

# Variable Keywords

| Keyword                    | Description             |
| -------------------------- | ----------------------- |
| `vars`                     | Play variables          |
| `hostvars`                 | Variables for all hosts |
| `group_names`              | Current host groups     |
| `groups`                   | Inventory groups        |
| `inventory_hostname`       | Current hostname        |
| `inventory_hostname_short` | Short hostname          |
| `ansible_play_hosts`       | Active hosts            |
| `ansible_play_batch`       | Current batch           |
| `ansible_check_mode`       | Check mode status       |
| `ansible_diff_mode`        | Diff mode status        |
| `omit`                     | Skip module parameter   |

---

# Built-in File Modules

| Module        | Description                  |
| ------------- | ---------------------------- |
| `copy`        | Copy files                   |
| `fetch`       | Retrieve remote files        |
| `template`    | Render Jinja2 templates      |
| `file`        | Manage files and directories |
| `stat`        | File information             |
| `find`        | Search files                 |
| `archive`     | Create archives              |
| `unarchive`   | Extract archives             |
| `assemble`    | Combine file fragments       |
| `lineinfile`  | Edit one line                |
| `blockinfile` | Manage text blocks           |
| `replace`     | Replace text                 |
| `slurp`       | Read binary file             |
| `tempfile`    | Create temporary files       |

---

# Package Modules

| Module          | Description                |
| --------------- | -------------------------- |
| `package`       | Generic package manager    |
| `apt`           | Debian packages            |
| `dnf`           | DNF packages               |
| `yum`           | YUM packages               |
| `apk`           | Alpine packages            |
| `pip`           | Python packages            |
| `package_facts` | Gather package information |

---

# Service Modules

| Module            | Description                |
| ----------------- | -------------------------- |
| `service`         | Generic service management |
| `systemd_service` | Manage systemd services    |
| `service_facts`   | Collect service facts      |

---

# Command Execution Modules

| Module    | Description                    |
| --------- | ------------------------------ |
| `command` | Execute command                |
| `shell`   | Execute shell command          |
| `script`  | Execute local script remotely  |
| `raw`     | Execute raw command            |
| `expect`  | Respond to interactive prompts |

---

# User and Group Modules

| Module           | Description         |
| ---------------- | ------------------- |
| `user`           | Manage users        |
| `group`          | Manage groups       |
| `authorized_key` | SSH authorized keys |
| `known_hosts`    | SSH known hosts     |

---

# System Modules

| Module     | Description            |
| ---------- | ---------------------- |
| `hostname` | Set hostname           |
| `reboot`   | Reboot system          |
| `setup`    | Gather facts           |
| `sysctl`   | Kernel parameters      |
| `timezone` | Configure timezone     |
| `cron`     | Manage cron jobs       |
| `at`       | Schedule one-time jobs |
| `mount`    | Mount filesystems      |
| `selinux`  | Configure SELinux      |

---

# Network Modules

| Module                | Description             |
| --------------------- | ----------------------- |
| `uri`                 | HTTP/HTTPS requests     |
| `get_url`             | Download files          |
| `wait_for`            | Wait for port or file   |
| `wait_for_connection` | Wait for SSH connection |

---

# Git and Source Control Modules

| Module       | Description             |
| ------------ | ----------------------- |
| `git`        | Manage Git repositories |
| `subversion` | Manage SVN repositories |

---

# Facts Modules

| Module          | Description       |
| --------------- | ----------------- |
| `setup`         | System facts      |
| `service_facts` | Service facts     |
| `package_facts` | Package facts     |
| `gather_facts`  | Collect all facts |

---

# Include Modules

| Module          | Description               |
| --------------- | ------------------------- |
| `include_tasks` | Include tasks dynamically |
| `import_tasks`  | Import tasks statically   |
| `include_role`  | Include role dynamically  |
| `import_role`   | Import role statically    |
| `include_vars`  | Load variables            |

---

# Debug Modules

| Module   | Description            |
| -------- | ---------------------- |
| `debug`  | Print variables        |
| `assert` | Validate conditions    |
| `fail`   | Force failure          |
| `pause`  | Pause execution        |
| `meta`   | Control play execution |

---

# Common Utility Modules

| Module         | Description           |
| -------------- | --------------------- |
| `set_fact`     | Create variables      |
| `add_host`     | Add inventory host    |
| `group_by`     | Create dynamic groups |
| `ping`         | Connectivity test     |
| `async_status` | Monitor async jobs    |

---

# Jinja2 Filters

| Filter          | Description          |
| --------------- | -------------------- |
| `default`       | Default value        |
| `length`        | Collection length    |
| `join`          | Join list            |
| `split`         | Split string         |
| `replace`       | Replace text         |
| `trim`          | Remove whitespace    |
| `upper`         | Uppercase            |
| `lower`         | Lowercase            |
| `title`         | Title case           |
| `capitalize`    | Capitalize           |
| `sort`          | Sort collection      |
| `unique`        | Remove duplicates    |
| `flatten`       | Flatten nested lists |
| `dict2items`    | Dictionary to list   |
| `items2dict`    | List to dictionary   |
| `combine`       | Merge dictionaries   |
| `to_json`       | Convert to JSON      |
| `from_json`     | Parse JSON           |
| `to_yaml`       | Convert to YAML      |
| `from_yaml`     | Parse YAML           |
| `regex_search`  | Regex search         |
| `regex_replace` | Regex replacement    |
| `basename`      | File basename        |
| `dirname`       | Directory name       |

---

# Jinja2 Tests

| Test          | Description         |
| ------------- | ------------------- |
| `defined`     | Variable exists     |
| `undefined`   | Variable missing    |
| `none`        | Value is null       |
| `string`      | Is string           |
| `number`      | Is numeric          |
| `mapping`     | Is dictionary       |
| `sequence`    | Is list             |
| `iterable`    | Is iterable         |
| `equalto`     | Equality comparison |
| `greaterthan` | Greater than        |
| `lessthan`    | Less than           |
| `match`       | Regex match         |
| `search`      | Regex search        |
| `version`     | Version comparison  |

---

# Loop Controls

| Keyword        | Description              |
| -------------- | ------------------------ |
| `loop`         | Iterate collection       |
| `loop_control` | Customize loop behavior  |
| `index_var`    | Loop index variable      |
| `label`        | Custom display label     |
| `pause`        | Delay between iterations |
| `extended`     | Extended loop variables  |

---

# Conditional Keywords

| Keyword              | Description              |
| -------------------- | ------------------------ |
| `when`               | Conditional execution    |
| `failed_when`        | Custom failure logic     |
| `changed_when`       | Custom change detection  |
| `ignore_errors`      | Ignore task failure      |
| `ignore_unreachable` | Ignore unreachable hosts |

---

# Inventory Plugins

| Plugin      | Description                |
| ----------- | -------------------------- |
| `host_list` | Comma-separated host list  |
| `ini`       | INI inventory              |
| `yaml`      | YAML inventory             |
| `script`    | External inventory script  |
| `auto`      | Automatic plugin detection |
| `toml`      | TOML inventory             |

---

# Connection Plugins

| Plugin         | Description               |
| -------------- | ------------------------- |
| `ssh`          | SSH connection            |
| `local`        | Execute locally           |
| `paramiko_ssh` | Paramiko SSH              |
| `psrp`         | PowerShell Remoting       |
| `winrm`        | Windows Remote Management |

---

# Strategy Plugins

| Plugin   | Description                 |
| -------- | --------------------------- |
| `linear` | Default sequential strategy |
| `free`   | Hosts execute independently |
| `debug`  | Interactive debugging       |

---

# Callback Plugins

| Plugin    | Description          |
| --------- | -------------------- |
| `default` | Standard output      |
| `minimal` | Minimal output       |
| `oneline` | Single-line output   |
| `tree`    | Save output per host |
| `junit`   | JUnit XML reports    |

---

# Lookup Plugins

| Plugin                | Description           |
| --------------------- | --------------------- |
| `env`                 | Environment variables |
| `file`                | Read local file       |
| `password`            | Generate password     |
| `pipe`                | Run local command     |
| `template`            | Render template       |
| `url`                 | Read URL              |
| `vars`                | Retrieve variables    |
| `inventory_hostnames` | Inventory host names  |

---

# Vault Commands

| Command          | Description           |
| ---------------- | --------------------- |
| `create`         | Create encrypted file |
| `edit`           | Edit encrypted file   |
| `encrypt`        | Encrypt file          |
| `decrypt`        | Decrypt file          |
| `encrypt_string` | Encrypt string        |
| `rekey`          | Change vault password |
| `view`           | View encrypted file   |

---

# Common Ad Hoc Options

| Option    | Description                |
| --------- | -------------------------- |
| `-i`      | Inventory file             |
| `-m`      | Module name                |
| `-a`      | Module arguments           |
| `-u`      | Remote user                |
| `-b`      | Become (sudo)              |
| `-K`      | Prompt for become password |
| `-k`      | Prompt for SSH password    |
| `-l`      | Limit hosts                |
| `-t`      | Tags                       |
| `--check` | Dry run                    |
| `--diff`  | Show differences           |
| `-f`      | Number of forks            |
| `-e`      | Extra variables            |
| `-v`      | Verbose output             |
| `-vv`     | More verbose               |
| `-vvv`    | Debug output               |
| `-vvvv`   | Connection debugging       |

# References
* [https://docs.ansible.com/ansible/latest/index.html](https://docs.ansible.com/ansible/latest/index.html)
