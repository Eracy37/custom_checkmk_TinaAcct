## custom_checkmk_TinaAcct
Shell Script for Tina job status (time Navigator by Atempo)

### Use
For use on checkmk put the script in ```/usr/var/lib/check_mk_agent/local```

You can add other type of job in this part of script :
```bash
if (vm == "") {
    if (folder ~ /host/) {
      # Key for agent
      key = "HOST|" platform
      platform_display = "HOST"
      vm_display = platform
    } else if (folder ~ /Nas/) {
      # Key for Nas
      key = "NAS|" platform
      platform_display = "NAS"
      vm_display = platform
    } else if (folder ~/.cat/) {
      # Key for catalog
      key = "CATALOG|" platform
      platform_display = "CATALOG"
      vm_display = platform
    }
```
If tina server is to slower you can put the script on crontab after put script in other location, create log with crontab and create another script for read file.
