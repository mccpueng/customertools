# Customer Tools
The viewFIleList will give you access to the files on each view.  The parameters passed will be:
viewfileList.ps -vip <cohesity cluster> -user <username> -domain <domain> -viewname <name of view> -showFiles (y/n) 
This will produce an excel spreadsheet that will have all the files and directory structure similiar to the output you shared with me for your paid tool.  

In addition to the viewFilelist script, you will need to download the cohesity-api.ps1 script.  Put both of these in the same directory and execute per the syntax above. 

I have added a script called viewStorageREport.ps1 the syntax of variables looks like:
viewStorageReport.ps1 -vip <cohesity cluster> -username <user> -domain <domain> -clustername <name of cluster> -smtpserver <optional mail server> -smptport <mail server port> -sendto <send to address> -Sendfrom <sendfrom> 

THe viewFIle list will help us understand what the actual file data is without snapshots and resillency impact nor storage reduction.  That will help us understand what the end data size should be after we do our pruning of archive data off  
