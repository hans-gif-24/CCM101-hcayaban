# ⚙️ Mission 9: The Cloud Automation Engineer

## Mission Overview

This laboratory focuses on automating routine server tasks using Bash scripting and Linux scheduling tools. I created a backup script, tested its execution, and configured a Cron Job to run the backup automatically every day at 2:00 AM.

## Objectives

- Understand the basics of Bash scripting and variables.
- Create and execute a backup script.
- Use `chmod` to allow script execution.
- Create a compressed backup using `tar`.
- Configure a Cron Job for automatic backups.
- Document the commands, results, and configuration in Markdown.

## Commands Executed

| Command | Purpose |
|---|---|
| `mkdir app-data` | Creates the sample application directory. |
| `echo "This is critical client data." > app-data/data.txt` | Creates a sample data file. |
| `nano backup.sh` | Creates or edits the backup script. |
| `cat backup.sh` | Displays the script contents. |
| `chmod +x backup.sh` | Allows the script to execute. |
| `./backup.sh` | Runs the backup script. |
| `ls -lh backups/` | Checks the generated backup files. |
| `crontab -l` | Displays the configured Cron Jobs. |
| `env EDITOR=nano crontab -e` | Opens the Cron configuration using Nano. |

## Skills Learned

- Bash shell scripting
- Linux file permissions
- File compression and backups
- Cron Job scheduling
- Linux command-line operations
- Technical documentation using Markdown

## Screenshots

The `screenshots/` folder contains evidence of the backup script execution and Cron Job configuration.

- `script-execution.png` — Successful execution of the backup script and generated backup file.
- `cron-schedule.png` — Configured Cron Job schedule.

## Results

The backup script executed successfully and created a timestamped compressed backup of the `app-data` directory. I also configured a Cron Job to run the script automatically every day at 2:00 AM.
