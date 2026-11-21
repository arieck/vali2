
Open Validation Server v2 is a free online service for validating IGC files, used by the FAI CIVL World XC Online Contest and many other national and international flying contests.

Prerequisites, recommended Installation: Install Apache2 + Perl on Windows 64bit platform

Q: What's the difference to Open Validation Server v3 Version ?
A: This Version here (v2) need only Perl CGI, while v3 requires PHP as well.

Q: Which version to choose if you want to implement your own Server ?
A: If you want to run just your own background service, lets say for LeonardoXC, then you are fine with vali2 from github. If you want to host the same public web interface like seen on vali.fai-civl.org, then you need a clone of vali3 from github, and modify the content to your needs.

Q: Can I create a pull request for changes here at GitHub ? For example for my own vali exe binary ?
A: No. Sorry. But you can clone the project and create your web service.
