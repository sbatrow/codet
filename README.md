# codet

# Schedule a reboot by using crontab
 Suppose you want to reboot the server at 2:05 am every day. Perform the following steps, adjusting the details to fit your requirements:

# Use the following command to edit the crontab file:
```
sudo crontab -e
```
To enter insert mode and add a new line at the end of the file, move the cursor to the last line and press the letter o.

In the blank line, add the following line to the file to set the desired daily execution time and command to execute:
```
05 02   *   *   *    /sbin/shutdown -r +5
```
Press Esc to exit insert mode and then enter :wq to save the file and quit crontab.

# Crontab example:
The following example shows the possible values for each element of a line in crontab.

# Example of job definition:
```
# .---------------- minute (0 - 59)
# |  .------------- hour (0 - 23)
# |  |  .---------- day of month (1 - 31)
# |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
# |  |  |  |  .---- day of week (0 - 6) (Sunday=0, Monday=1, and so on)
# |  |  |  |  |
# *  *  *  *  * user-name  command-to-be-executed
```
