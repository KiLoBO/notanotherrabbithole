I personally use X11 forwarding (over ssh) to use GUI tools on my remote hosted kali machine wihout a bunch of proxies. Using the -X switch when initially remoting into the machine will run the tools' windows on the ssh client's desktop, but the networking and data will all stay on the remote host. 

In my personal scenario as laid out above, I SSH into a remote hosted Kali VM from my linux desktop. However this can be done with windows, which I will get into at the end of this page. 

## The setup 
On Kali:
  - Make sure ssh.service is up and running (helps to just enable it so it will always start for you) `sudo systemctl status/start/enable ssh.service`

## Initial Connection
`ssh -X user@ip`
  - The -Y switch can also be used for a "trusted X forwarding session" however there isn't any real security enhancements over just using the -X switch over ssh.

## The Fun Stuff
Now run any tool you want with their CLI command! Keep in mind, running it will take the entire terminal up so be sure to background the process in the command and/or use screens.
![burpforwarded](https://i.imgur.com/iQc7j85.png)
