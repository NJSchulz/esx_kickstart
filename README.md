# ESX Multi-host Kickstart script with Menu
This kickstart script presents a menu of different hosts and then installs a particular personality based on the menu selection.


## Notes
I serve this file via Apache2 with HTTP in my lab. To ensure proper delivery, I installed the mod_headers module and added a directive to my site's configuration file that sets the Content-Disposition header, thereby enabling the download of the file rather than simply displaying it.

To enable the mod_headers: `sudo a2enmod headers`

Added the following to the sites-available conf file:
```
<Files *>
     ForceType application/octet-stream
     Header set Content-Disposition "attachment"
 </Files>
```
