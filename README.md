# Apple-Profile-Manager-Report
Reporting the Profile manager devices


Usage:

Copy all files to /PATHTOYOURWEBSITEFOLDER


You will need to export the data from Profile Manager


sudo -u _devicemgr psql -U _devicemgr -d devicemgr_v2m0 -h /Library/Server/ProfileManager/Config/var/PostgreSQL 


then


\copy (select "DeviceName","SerialNumber","ProductName","mdm_target_type","OSVersion","IMEI","last_checkin_time","IsSupervised","activation_lock_bypass_code","last_push_time" from devices) to '/PATHTOYOURWEBSITEFOLDER/ProfileManagerReport.csv' (format csv, delimiter ';’)


Edit the relevant info in the index.html file

Example:

https://github.com/djquazzi/Apple-Profile-Manager-Report/blob/master/pm.png
