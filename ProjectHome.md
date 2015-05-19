bltool offers a way to control your display backlight when other tools such as xbacklight and e17 fail to.

It just uses normal sysfs or xrandr interfaces, the same as xbacklight and e17 and other things. The primary difference is bltool offers more configurability through environment variables and through the fact that it is a script instead of a compiled binary. It works in at least some situations where the normal programs fail.

It can be used in non-interactive, cli, curses-ui and gtk-gui modes.

It can be used both with and without any X server or display.

Currently implemented as a bash script that uses zenity for gui, dialog for curses ui, and uses the standalone xrandr program for any xrandr actions. For sysfs it just reads/writes directly. No external programs like dialog or zenity or xrandr are needed if you use sysfs mode and specify the sysfs directory name via ~/.bltool config file or environment variables, and specify the desired brightness level with the -, +, or 0-100 command line arguments.

[Download current version](http://bltool.googlecode.com/svn/trunk/bltool)