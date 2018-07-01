# powerless
Powersaving Tool for Thinkpad E550

## Installation
1. Add user to "video" group
2. Install systemd service using
* sudo cp systemd/backlight* /etc/systemd/system
* sudo systemctl enable backlight.service
* sudo systemctl start backlight.service
3. Adjust backlight sys-path in powerlessd for your system
4. Add powerlessd as startup application to your WM (e.g. Gnome session)

This is a prototype - only use it with care for one single user on your system

## Usage
Just start it. You can specify the following options:

-f                : start in foreground mode (no daemonization)

-minblight <value>: specify level of darkness if dimmed, value depends on 
                    /sys/class/backlight/intel_backlight/max_brightness

-idletime <value> : amount of seconds before to dim
