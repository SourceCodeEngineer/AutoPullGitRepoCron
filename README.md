# How to automatically pull any Github repository you have access to

# Script

Download the given [script](gitpull.sh) in this repository to any location of your choosing and make it via "chmod +x gitpull.sh" executable!

# Crontab

Crontab is essential but there are possibilities without it (`not covered here`).
If you haven't installed crontab yet and it is not preinstalled then do so by the following command:
    `sudo apt-get install cron-apt`
    
After you have successfully installed crontab we will switch to the root user.
To switch to the root user you can just type `sudo -s` into the shell and confirm with your sudoers password.

Now that we are logged in as the root user we can switch directory to the `/root` folder via `cd /root`.

If there is no directory `log/` then create one with `mkdir log`.

Now that we confirmed we have a directory where the logs get stored we can edit the crontab to our liking. For this to happen we type into the command line the following command:

`rontab -e`

If you do this for the first time, it will ask you what editor to select. Select the on of your liking!

