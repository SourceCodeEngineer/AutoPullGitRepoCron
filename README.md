# How to automatically pull your Github repository

## Script

Download the given [script](gitpull.sh) in this repository to any location of your choosing and make it via `chmod +x gitpull.sh` executable!

## Crontab

### Installation
Crontab is essential but there are possibilities without it (`not covered here`).
If you haven't installed crontab yet and it is not preinstalled then do so by the following command:
    `sudo apt-get install cron-apt`

### Logs
After you have successfully installed crontab we will switch to the root user.
To switch to the root user you can just type `sudo -s` into the shell and confirm with your sudoers password.

Now that we are logged in as the root user we can switch directory to the `/root` folder via `cd /root`.

If there is no directory `log/` then create one with `mkdir log`.

### Setup
Now that we confirmed we have a directory where the logs get stored we can edit the crontab to our liking. For this to happen we type into the command line the following command: `crontab -e`

If you do this for the first time, it will ask you what editor to select. Select the on of your liking!

Now that we are editing the crontab file, we can now copy paste the following command:
    `* * * * * cd /PATH_TO_EXECUTABLE_SCRIPT && ./gitpull.sh > /root/log/gitpull-script.log  2>&1 &`
You can edit this command to your liking, it is currently set to automatically pull `EVERY MINUTE` which is because it is a template.
If you want to change the time of it then you can just overwrite the stars and if you are not sure you did it write you can check it [here](https://www.crondrive.com/test-cron-expression?expression=0+2+%2A+%2A+%2A).

Save the file and it should run automatically.
