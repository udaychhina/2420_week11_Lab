# ACIT 2420 WEEK 11 Lab

## Backup

### Team Members

- *Uday Chhina*
- *Simon Freeman*

## Backup

Creates and updates backups of specified directories from server-one into the backup-server every friday at 01:00.

### backup

1. Create a directory in /opt by using sudo mkdir /opt/backup
2. Save backup file into /opt/backup  
    - **SSH key** should match the SSH key of **your own backup server**. This is to be specified in the script, inside the section with double quotes. 
    - **The user and host** should also be specified inside the `rsync` command:
Example:
![backup](./images/backup.png)

### backup_config

1. Create file inside the /opt/backup-script directory
2. Specify the directories to backup and the ip of backup-server
    - IP should match the **IP of your own backup server**, and directories should match the path of **directories you wish to backup**

### backup.service

1. Place the file in /etc/systemd/system    
2. To enable the service, use `systemctl enable backup-service.service` 
3. To start  the service, use `systemctl start backup-service.service`
4. Verify the service is active with `systemctl status backup-service.service`
- if successful, systemctl status should look like screenshot below:

### backup.timer
1. Place the file in /etc/systemd/system    
2. To enable the service, use `systemctl enable backup-timer.timer` 
3. To start  the service, use `systemctl start backup-timer.timer`
4. Verify the service is active with `systemctl status backup-timer.timer`
- if successful, systemctl status should look like screenshot below:

## Weather Script

Retrieves the weather forecast in Vancouver every day at 05:00

### weather
Place the script in /opt/weather

### weather.service
1. Place the file in /etc/systemd/system    
2. To enable the service, use `systemctl enable weather.service` 
3. To start  the service, use `systemctl start weather.service`
4. Verify the service is active with `systemctl status weather.service`
- if successful, systemctl status should look like screenshot below:

### weather.timer
1. Place the file in /etc/systemd/system    
2. To enable the service, use `systemctl enable weather.timer` 
3. To start  the service, use `systemctl start weather.timer`
4. Verify the service is active with `systemctl status weather.timer`
- if successful, systemctl status should look like screenshot below:
