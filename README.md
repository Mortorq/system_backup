# system_backup
The system_backup tool is a software written in python to make regular backups of a Linux system

This script is made for automated backups of a linux system (tested with Debian and Ubuntu). On the last day of the Week (Sunday) it should make a full backup of the whole system, excluding the directories listed in the key exclude_dirs of backup_config, removing/creating a new metadata file on which all incremental backups in the following week will rely on.

The backups will be removed automated in a defined cicle, the default is 4 days. Configurable in the "backups_to_keep" key of backup_config. This means if the first Backup was written on a Monday, this backup will be deleted on a friday. The script detects the oldest backup and removes it without questioning.

Todos:

- Maybe the configuration parameters should also be configurable via parameters given to the script
- implement a differential backup; make a swith for differential and incremental in the script
