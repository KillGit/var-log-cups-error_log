# var-log-cups-error_log

tail -f error_log:
================================================================================================================
W [17/May/2016:06:47:46 -0700] Notifier for subscription 4 (dbus://) went away, retrying!
E [17/May/2016:06:47:46 -0700] File "/usr/lib/cups/notifier/dbus" has insecure permissions (0100777/uid=0/gid=0).
W [17/May/2016:06:47:46 -0700] Notifier for subscription 4 (dbus://) went away, retrying!
E [17/May/2016:06:47:46 -0700] File "/usr/lib/cups/notifier/dbus" has insecure permissions (0100777/uid=0/gid=0).
W [17/May/2016:06:47:46 -0700] Notifier for subscription 4 (dbus://) went away, retrying!
================================================================================================================

SOLVED&STOP creating this big file. 


sudo stop cups
sudo rm /etc/cups/subscriptions.conf*
sudo rm -r /var/cache/cups
sudo start cups
sudo rm -r /var/log/cups/error_log
