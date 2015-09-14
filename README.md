# system_backup
The system_backup tool is a software written in python to make regular backups of a Linux system

In it's current state it can make backups of every regular business day (monday - friday). From monday to thursday it makes backups for every file that was change within the last 24h. On Friday it makes a full backup of the system.
A dict with dirs to exclude is implemented and shall be modified for personal preferences.

Todos:

- All the parameters should be given to the script and shouldn't be hardcoded
- implement a real differential and incremental backup function


NOTE:
Most of the code is not written by me. The original code is from Josh Kapple; http://www.joshkapple.com/blog/2010/05/23/easy-linux-backup-script-with-python/ . I just did some useful modifikations / improvements
