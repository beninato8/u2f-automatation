# u2f-automatation

## A bit of code to enable software only login to a site that requires u2f authorization

#### You need a U2F HID emulator for this to work, like GitHub's [SoftU2F](https://github.com/github/SoftU2F)

 - [Applescript](mfa-autoclick.scpt) to click the notification from [SoftU2F](https://github.com/github/SoftU2F)
 - [Applescript as text](mfa-click.txt) is `cat`ed and piped into `osascript`
 - [Shell script](mfa-click) runs in background
   - I use zsh, and run the script using `./mfa-click 2&>1 > /dev/null/ &|`
   - You can probably run it with bash as well, using instructions from [here](https://unix.stackexchange.com/questions/3886/difference-between-nohup-disown-and)