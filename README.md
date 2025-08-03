# GoPanel
GoPanel Free Linux Web Hosting Control Panel
<br><br>

<a href='https://google.com'>Goo</a>


**GoPanel Website:**
<br>
https://www.gopanel.org
<br><br>

**Install GoPanel via command line:**
<br>
curl -s -o latest -L https://download.gopanel.org && chmod +x latest && ./latest
<br><br>

**GoPanel Demo:**
<br>
https://go.w75.net
<br><br>

**How to Encrypt PHP Code (Warring: All files in domain will be encrypted)?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/encoder Domain Key
<br>
Example:
<br>
/go/encoder blackhost.com mypassword
<br>

**How to Restore Full cPanel Backup via GoPanel?**
<br>
The first method is to restore the full cPanel backup via GoPanel. Of course, in order to be able to restore the backup using this method you need to have root access to GoPanel which is listening on port 2020. So if your domain is example.com, you can access GoPanel via web browser at http://example.com:2020.
<br>
Once you log in to GoPanel, navigate to Backups and then select Restore a Full Backup. This GoPanel feature will allow you to restore specific backup with File.
<br>
To restore with file, you must upload the full cPanel backup file to the following directory:
<br>
/backup
<br>
<br>
<b>Restore Full cPanel Backup via command line</b>. Yes, this is another method which some server admins find much easier than the first one. For this method you need to have SSH access to the server. Connect to your Linux server via SSH and run the following command as root:
<br>
/go/restore example
<br>
Of course, you need to replace example with the actual cPanel username or filename.tar.gz for the account you want to restore. Also, make sure that the full cPanel backup is properly uploaded in the /backup directory on your server before starting the restoration process.
<br>

**How to backup GoPanel accounts from one server to another GoPanel server?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/backup all full scp RemoteIP root RemotePassword 22 /backup
<br>
or
<br>
/go/backup all RemoteIP RemotePassword
<br>

**How to transfer GoPanel accounts from one server to another GoPanel server?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/copy Domain RemoteIP RemotePassword
<br>
To copy all accounts:
<br>
/go/copy all RemoteIP RemotePassword
<br>

**How to Backup & Migrate GoPanel Server with All Configurations?**
<br>
Setting Up a Fresh Remote GoPanel Server Without Websites, Just Install GoPanel
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/clone RemoteIP RemotePassword
<br>

**How to copy GoPanel backup file from one server to another GoPanel server?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/scp filename.tar.gz RemoteIP RemotePassword
<br>
Or
<br>
/go/scp all RemoteIP RemotePassword
<br>
**How to Copy Folder from GoPanel Server to Remote Backup Server(Storage Box)?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/backup &ltLocal Folder Path&gt &ltRemote Folder Path&gt
<br>
Example:
<br>
/go/backup /home/ /backup/home/
<br>
(Setup Schedule Backup Required via Dashboard)
<br>

**How to Restore Folder from Remote Backup Server(Storage Box) to Local GoPanel Server?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/restore &ltRemote Folder Path&gt &ltLocal Folder Path&gt 
<br>
Example:
<br>
/go/restore /backup/home/ /home/
<br>

**How to Restore Account from Remote Backup Server(Storage Box) to Local GoPanel Server?**
<br>
Connect to your Linux server (Local Server) via SSH and run the following command as root:
<br>
/go/restore Domain BackupDate
<br>
Example:
<br>
/go/restore blackhost.com 2023-01-30
<br>

**How to Copy Database from Current Server to Another?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/copydatabase DatabaseName RemoteIP RemotePassword
<br>

**How to Copy Database Table from Current Server to Another?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/copytable DatabaseName TableName RemoteIP RemotePassword
<br>
**How to Convert Database from MyISAM  to InnoDB?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/myisam2innodb DatabaseName
<br>
**How to Convert Table from MyISAM  to InnoDB?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/myisam2innodb DatabaseName TableName

**How to re-sorting id column in a MySQL table (Both PRIMARY KEY and AUTO INCREMEN)?**
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/reid DatabaseName TableName
<br>
**How do I switch between NGINX and Apache web server?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
<b>Switch to NGINX:</b>
<br>
/go/nginx
<br>
<b>Switch to Apache:</b>
<br>
/go/apache
<br>

**How to Install an SSL Certificate on a Domain?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/ssl domain.com
<br>

**How to Install an SSL Certificate for all domains?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/ssl all
<br>
<br>
To Check SSL Certificate Run:
<br>
/go/checkssl
<br>

**How do I force a new SSL certificate?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/ssl all --force
<br>
**How to install PHP 7.1 and PHP 7.2 and all neccessary extensions?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/installphp 7.1
<br>
/go/installphp 7.2
<br>

**How to set Default PHP Version in GoPanel?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/defaultphp 7.4
<br>
php -v
<br>
**How to Solve 502 Bad Gateway Issues?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/conf
<br>
If the problem still persists run:
<br>
/go/reinstall
<br>

**How to Increase Websites Speed?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/resolver OpenDNS
<br>
<br>
/go/index
<br>
Wait 5 minutes then run:
<br>
/go/index
<br>

**Slow performance after securing websites with Lets Encrypt SSL**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/resolver
<br>
or
<br>
/go/resolver OpenDNS
<br>
or
<br>
/go/resolver Cloudflare
<br>

**How do I access my webmail?**
<br>
<b>Steps for logging into webmail</b>
<ol>
<li>Visit example.com/webmail. Be sure to replace example.com with your actual domain name.</li>
<li>Choose Roundcube or RainLoop or SquirrelMail as your default client.</li>
<li>Enter your username and password, and then click login. User Name: Enter your full email address, all lower case.</li>
<li>You should now be logged in!</li>
</ol>
<br>

**How to change default SMTP port (25) in GoPanel?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/smtp 26
<br><br>
How do I get back to default settings?
<br>
/go/smtp 25
<br>

**How do I Update Roundcube?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/roundcube
<br><br>
How to Downgrade Roundcube?
<br>
/go/roundcube 1.3.9
<br>

**How to Install SquirrelMail on GoPanel?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/squirrelmail
<br>

**How to set limitations for outgoing email?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/smtplimit 30

<br><br>
30 emails per hour / user
<br>

**How To Get Emails Delivered to Inbox?**
<br>
To send emails and avoid them being classified as spam 
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/checksmtp
<br>

**How to detect which account is sending spam?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/spam now
<br>
<br>
To get the mail queue count:
/go/spam count
<br>

**How to Install ionCube Loader in GoPanel?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/ioncube
<br>

**How to Install GoPanel on Google Compute Engine (GCP) or (AWS)?**
<br>
Connect to your Linux (GCP) or (AWS) via SSH (Web Browsing) and run the following command:
<br>
Change the root password:
<br>
sudo passwd
<br>
Login as root:
<br>
su
<br>
Start Install GoPanel:
<br>
curl -s -o latest -L https://download.gopanel.org && chmod +x latest && ./latest
<br>
**How to Install Gdown in GoPanel?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/gdown
<br>
<br>
How to download a folder from google drive using terminal?
<br>
gdown --folder --id &ltfolder_id&gt
<br><br>
How to download a file from google drive using terminal?
<br>
gdown --id &ltfile_id&gt
<br>
**How do I set up nameservers?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/nameservers ns1.domain.com ns2.domain.com
<br>
**What does resetting a DNS zone do?**
<br>
If you add/delete DNS records and want to revert back to the original DNS, you can Reset the DNS Zone. This will remove all your custom DNS records and create the standard records for your domain.
<br>
<br>
**How to Reset a DNS Zone in GoPanel?**
<br>
To reset zone for a domain
<br>
/go/zone domain.com reset
<br>

<br>
To reset zone for all domains
<br>
/go/zone all reset
<br>

**How do I upload files to my website?**
<br>
You must either use FTP (file transfer protocol) client (<a href='https://www.gopanel.org/download/gopanel-ftp.exe'>Download GoPanel-FTP</a>), or upload via our File Manager located in your members' area. <b>www</b> is the only folder of which content is accessible to the browser, therefore all your website content must be uploaded there.
<br>
<br>
Also, there must be a file named index.htm, index.html or index.php inside <b>www</b> directory for site to be working properly.
<br>
**How to Rebuild the Apache Configuration?**
<br>
To rebuild the Apache configuration file, run the following command as root:
<br>
/go/conf
<br>

**How to Reinstall Apache or NGINX?**
<br>
To reinstall Apache or NGINX, run the following command as root:
<br>
/go/server
<br>
**Detecting and Resolving Server Problems**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/conf
<br>
If the problem still persists run:
<br>
/go/reinstall
<br>

**How do you remove invalid email addresses from your email campaign list?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/undelivered
<br>
<br>
1- Navigate to the GoPanel's Undelivered Emails interface (GoPanel >> Home >> Email >> Undelivered Emails).
<br>
2- Click Export as CSV
<br>
3- Remove Invalid Email Addresses from Mailing List
<br>

**How do I delete undelivered emails?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/undelivered all
<br>
Or
<br>
/go/undelivered domain.com
<br>

**How do I set Date and time automatically in GoPanel?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/timezone
<br><br>
How do I set DST time?
<br>
/go/dst
<br>
**How do I track bots in GoPanel?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/bot
<br>
**How do I delete undelivered emails?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/undelivered delete
<br>

**How can I check if port 25 is open?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/checkmail
<br>
**How do I solve a \"Connection Refused\" error?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/connect

**How to stop getting spam emails on GoPanel?**
<br>
Configure IP filter rules to block about (1M) Blacklist IP Addresses. Blacklist IP updated every 2 hours.
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/junk
<br>
**How to Block Bad Bots on Your Server?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/blacklist

**How can I determine the source IP of a DDOS attack?**
<br>
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/ddos
<br>
**How to import a single table from a dump file in MySQL?**
Connect to your Linux server via SSH and run the following command as root:
<br>
/go/table -f file.sql -t TableName -o out.sql
<br>
mariadb DatabaseName < out.sql
<br>
**How can I get the 10 most frequently executed SQL queries?**
<br>
This command will return the 10 most frequently executed SQL queries.
<br>
/go/querytop
<br>
**How can I get the SQL queries that are currently running on my MariaDB or MySQL server?**
This will show only the active queries that are currently being executed and exclude idle connections.
<br>
/go/mysqltop
<br>
**How can I monitor web server traffic in real-time on Apache?**
<br>
You can use HTTPTOP to monitor web server traffic in real time. It provides an interactive, real-time view of Apache log files, displaying detailed statistics on incoming requests, traffic patterns, and server performance. This tool helps in quickly identifying high-traffic URLs, status codes, request counts, and server health.
<br>
/go/httptop

**How can I change the Browser Cache TTL on Cloudflare?**
<br>
To change the Browser Cache TTL on Cloudflare using the API via command line, you can use the following:
<br>
/go/cloudflare all browser 3600
<br>
**How can I solve the \"Too many certificates\" error in Let's Encrypt?**
To solve the \"Too many certificates\" error in Let's Encrypt using the command line, you can follow these steps:
<br>
/go/ssl all --buypass
<br>
/go/ssl all --limit
<br>
**How do I migrate my database from MySQL/MariaDB to PostgreSQL?**
<br>
Converting from MySQL/MariaDB to PostgreSQL
<br>
mariadb-dump database_name > db.sql
<br>
/go/mariadb2postgre db.sql
<br>
PGPASSWORD=\"password\" psql -h localhost -U database_username -d database_name -f db.sql



