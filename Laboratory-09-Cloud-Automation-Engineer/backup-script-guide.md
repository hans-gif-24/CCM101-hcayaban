# Backup Script Guide

## 1. Purpose of the Script

The Bash script automates the backup of the `app-data` folder. It creates a timestamped compressed archive and saves it inside the `backups` folder.

## 2. Backup Script

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## 3. File Permissions

The command `chmod +x backup.sh` gives the script permission to execute. Without this permission, running `./backup.sh` may result in a `Permission denied` error.

After changing the permission, the script can be executed using:

```bash
./backup.sh
```

## 4. Cron Job Configuration

The following Cron expression schedules the backup script to run every day at 2:00 AM.

```bash
0 2 * * * /root/backup.sh
```

### Cron Expression Breakdown

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | At minute 0 |
| Hour | `2` | At 2 AM |
| Day of Month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |

The command below displays the configured Cron Jobs:

```bash
crontab -l
```

## 5. Commands Used

| Command | Purpose |
|---|---|
| `mkdir` | Creates a directory. |
| `echo` | Displays text or writes text to a file. |
| `nano` | Creates or edits a file in the terminal. |
| `cat` | Displays file contents. |
| `chmod +x` | Allows a script to execute. |
| `./backup.sh` | Executes the backup script. |
| `mkdir -p` | Creates a directory if it does not exist. |
| `tar -czf` | Creates a compressed archive. |
| `ls -lh backups/` | Lists backup files and their sizes. |
| `crontab -e` | Edits scheduled Cron tasks. |
| `crontab -l` | Displays scheduled Cron tasks. |

## 6. Result

The backup script ran successfully and created a timestamped `.tar.gz` archive of the `app-data` folder. The Cron Job was also configured to execute the backup script automatically every day at 2:00 AM, according to the system's time and timezone.
