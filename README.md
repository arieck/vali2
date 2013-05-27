Open Validation Server v2 is a free online service for validating IGC files, 
used by the FAI CIVL World XC Online Contest and many other national and international flying contests. 
More details, and a running version at http://vali.fai-civl.org/

Prerequisites, recommended Installation:

1)Installed Apache2 + Perl on Windows 32bit platform
  for example using xampp on Windows 7 or Windows 2008
  see www.apachefriends.org/en/xampp.html‎
  
2)configure the httpd.conf accordingly, for example:

Listen 80
DocumentRoot "C:/wwwroot/vali"
<Directory "C:/wwwroot/vali">
    Options Indexes FollowSymLinks Includes ExecCGI
    AllowOverride All
	Order allow,deny
	Allow from all
    Require all granted	
</Directory>
<Directory "C:/wwwroot/vali/cgi-bin">
    AllowOverride All
    Options Indexes FollowSymLinks Includes ExecCGI
	Order allow,deny
	Allow from all
    Require all granted
</Directory>

3)deploy the valiserver files at your webserver document root directory

4) configure the vali-igc.conf for the following directory variables
ModuleDir, LogDir

5) configure the cgi-bin/vali-igc.cgi for the following directory variables
DIR_CONF, DIR_IGCUPLOAD

6) configure the shebang line at cgi-bin/vali-igc.cgi to use your Perl installation

7)Test it, using CURL client
$ /usr/bin/curl -F igcfile=@sample-xgd.igc  yourserver.domain.tld/cgi-bin/vali-igc.cgi
or use your Web Browser for testing 
http://yourserver.domain.tld/test-vali2.html

Notes:
To install a new vali.exe, simply add a new Module to vali-igc.conf

Tip:
When you use and install xampp at c:\xampp and use c:\wwwroot\vali 
as your document root, then you just need to configure the Apache httpd.conf

