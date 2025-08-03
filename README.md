# gopanel
GoPanel Free Linux Web Hosting Control Panel

Install GoPanel via command line:
curl -s -o latest -L https://download.gopanel.org && chmod +x latest && ./latest





How to Encrypt PHP Code (Warring: All files in domain will be encrypted)?
Connect to your Linux server via SSH and run the following command as root:
/go/encoder Domain Key
Example:
/go/encoder blackhost.com mypassword
How to Restore Full cPanel Backup via Go Panel?
The first method is to restore the full cPanel backup via Go Panel. Of course, in order to be able to restore the backup using this method you need to have root access to Go Panel which is listening on port 2020. So if your domain is example.com, you can access Go Panel via web browser at http://example.com:2020.
Once you log in to Go Panel, navigate to Backups and then select Restore a Full Backup. This Go Panel feature will allow you to restore specific backup with File.
To restore with file, you must upload the full cPanel backup file to the following directory:
/backup

Restore Full cPanel Backup via command line. Yes, this is another method which some server admins find much easier than the first one. For this method you need to have SSH access to the server. Connect to your Linux server via SSH and run the following command as root:
/go/restore example
Of course, you need to replace example with the actual cPanel username or filename.tar.gz for the account you want to restore. Also, make sure that the full cPanel backup is properly uploaded in the /backup directory on your server before starting the restoration process.
How to backup Go Panel accounts from one server to another Go Panel server?
Connect to your Linux server via SSH and run the following command as root:
/go/backup all full scp RemoteIP root RemotePassword 22 /backup
or
/go/backup all RemoteIP RemotePassword
How to transfer Go Panel accounts from one server to another Go Panel server?
Connect to your Linux server via SSH and run the following command as root:
/go/copy Domain RemoteIP RemotePassword
To copy all accounts:
/go/copy all RemoteIP RemotePassword
How to Backup & Migrate Go Panel Server with All Configurations?
Setting Up a Fresh Remote Go Panel Server Without Websites, Just Install Go Panel
Connect to your Linux server via SSH and run the following command as root:
/go/clone RemoteIP RemotePassword
How to copy Go Panel backup file from one server to another Go Panel server?
Connect to your Linux server via SSH and run the following command as root:
/go/scp filename.tar.gz RemoteIP RemotePassword
Or
/go/scp all RemoteIP RemotePassword
How to Copy Folder from Go Panel Server to Remote Backup Server(Storage Box)?
Connect to your Linux server via SSH and run the following command as root:
/go/backup <Local Folder Path> <Remote Folder Path>
Example:
/go/backup /home/ /backup/home/
(Setup Schedule Backup Required via Dashboard)
How to Restore Folder from Remote Backup Server(Storage Box) to Local Go Panel Server?
Connect to your Linux server via SSH and run the following command as root:
/go/restore <Remote Folder Path> <Local Folder Path>
Example:
/go/restore /backup/home/ /home/
How to Restore Account from Remote Backup Server(Storage Box) to Local Go Panel Server?
Connect to your Linux server (Local Server) via SSH and run the following command as root:
/go/restore Domain BackupDate
Example:
/go/restore blackhost.com 2023-01-30
How to Copy Database from Current Server to Another?
Connect to your Linux server via SSH and run the following command as root:
/go/copydatabase DatabaseName RemoteIP RemotePassword
How to Copy Database Table from Current Server to Another?
Connect to your Linux server via SSH and run the following command as root:
/go/copytable DatabaseName TableName RemoteIP RemotePassword
How to Convert Database from MyISAM to InnoDB?
Connect to your Linux server via SSH and run the following command as root:
/go/myisam2innodb DatabaseName
How to Convert Table from MyISAM to InnoDB?
Connect to your Linux server via SSH and run the following command as root:
/go/myisam2innodb DatabaseName TableName
How to re-sorting id column in a MySQL table (Both PRIMARY KEY and AUTO INCREMEN)?
Connect to your Linux server via SSH and run the following command as root:
/go/reid DatabaseName TableName
How do I switch between NGINX and Apache web server?
Connect to your Linux server via SSH and run the following command as root:
Switch to NGINX:
/go/nginx
Switch to Apache:
/go/apache
How to Install an SSL Certificate on a Domain?
Connect to your Linux server via SSH and run the following command as root:
/go/ssl domain.com
How to Install an SSL Certificate for all domains?
Connect to your Linux server via SSH and run the following command as root:
/go/ssl all

To Check SSL Certificate Run:
/go/checkssl
How do I force a new SSL certificate?
Connect to your Linux server via SSH and run the following command as root:
/go/ssl all --force
How to install PHP 7.1 and PHP 7.2 and all neccessary extensions?
Connect to your Linux server via SSH and run the following command as root:
/go/installphp 7.1
/go/installphp 7.2
How to set Default PHP Version in GoPanel?
Connect to your Linux server via SSH and run the following command as root:
/go/defaultphp 7.4
php -v
How to Solve 502 Bad Gateway Issues?
Connect to your Linux server via SSH and run the following command as root:
/go/conf
If the problem still persists run:
/go/reinstall
How to Increase Websites Speed?
Connect to your Linux server via SSH and run the following command as root:
/go/resolver OpenDNS

/go/index
Wait 5 minutes then run:
/go/index
Slow performance after securing websites with Lets Encrypt SSL
Connect to your Linux server via SSH and run the following command as root:
/go/resolver
or
/go/resolver OpenDNS
or
/go/resolver Cloudflare
How do I access my webmail?
Steps for logging into webmail
Visit example.com/webmail. Be sure to replace example.com with your actual domain name.
Choose Roundcube or RainLoop or SquirrelMail as your default client.
Enter your username and password, and then click login. User Name: Enter your full email address, all lower case.
You should now be logged in!
How to change default SMTP port (25) in Go Panel?
Connect to your Linux server via SSH and run the following command as root:
/go/smtp 26

How do I get back to default settings?
/go/smtp 25
How do I Update Roundcube?
Connect to your Linux server via SSH and run the following command as root:
/go/roundcube

How to Downgrade Roundcube?
/go/roundcube 1.3.9
How to Install SquirrelMail on Go Panel?
Connect to your Linux server via SSH and run the following command as root:
/go/squirrelmail
How to set limitations for outgoing email?
Connect to your Linux server via SSH and run the following command as root:
/go/smtplimit 30

30 emails per hour / user
How To Get Emails Delivered to Inbox?
To send emails and avoid them being classified as spam
Connect to your Linux server via SSH and run the following command as root:
/go/checksmtp
How to detect which account is sending spam?
Connect to your Linux server via SSH and run the following command as root:
/go/spam now

To get the mail queue count: /go/spam count
How to Install ionCube Loader in Go Panel?
Connect to your Linux server via SSH and run the following command as root:
/go/ioncube
How to Install Go Panel on Google Compute Engine (GCP) or (AWS)?
Connect to your Linux (GCP) or (AWS) via SSH (Web Browsing) and run the following command:
Change the root password:
sudo passwd
Login as root:
su
Start Install Go Panel:
curl -s -o latest -L https://download.gopanel.org && chmod +x latest && ./latest
How to Install Gdown in Go Panel?
Connect to your Linux server via SSH and run the following command as root:
/go/gdown

How to download a folder from google drive using terminal?
gdown --folder --id <folder_id>

How to download a file from google drive using terminal?
gdown --id <file_id>
How do I set up nameservers?
Connect to your Linux server via SSH and run the following command as root:
/go/nameservers ns1.domain.com ns2.domain.com
What does resetting a DNS zone do?
If you add/delete DNS records and want to revert back to the original DNS, you can Reset the DNS Zone. This will remove all your custom DNS records and create the standard records for your domain.

How to Reset a DNS Zone in Go Panel?
To reset zone for a domain
/go/zone domain.com reset

To reset zone for all domains
/go/zone all reset
How do I upload files to my website?
You must either use FTP (file transfer protocol) client (Download Go Panel-FTP), or upload via our File Manager located in your members' area. www is the only folder of which content is accessible to the browser, therefore all your website content must be uploaded there.

Also, there must be a file named index.htm, index.html or index.php inside www directory for site to be working properly.
How to Rebuild the Apache Configuration?
To rebuild the Apache configuration file, run the following command as root:
/go/conf

How to Reinstall Apache or NGINX?
To reinstall Apache or NGINX, run the following command as root:
/go/server
Detecting and Resolving Server Problems
Connect to your Linux server via SSH and run the following command as root:
/go/conf
If the problem still persists run:
/go/reinstall
How do you remove invalid email addresses from your email campaign list?
Connect to your Linux server via SSH and run the following command as root:
/go/undelivered

1- Navigate to the GoPanel's Undelivered Emails interface (GoPanel >> Home >> Email >> Undelivered Emails).
2- Click Export as CSV
3- Remove Invalid Email Addresses from Mailing List
How do I delete undelivered emails?
Connect to your Linux server via SSH and run the following command as root:
/go/undelivered all
Or
/go/undelivered domain.com
How do I set Date and time automatically in GoPanel?
Connect to your Linux server via SSH and run the following command as root:
/go/timezone

How do I set DST time?
/go/dst
How do I track bots in GoPanel?
Connect to your Linux server via SSH and run the following command as root:
/go/bot
How do I delete undelivered emails?
Connect to your Linux server via SSH and run the following command as root:
/go/undelivered delete
How can I check if port 25 is open?
Connect to your Linux server via SSH and run the following command as root:
/go/checkmail
How do I solve a "Connection Refused" error?
Connect to your Linux server via SSH and run the following command as root:
/go/connect
How to stop getting spam emails on Go Panel?
Configure IP filter rules to block about (1M) Blacklist IP Addresses. Blacklist IP updated every 2 hours.
Connect to your Linux server via SSH and run the following command as root:
/go/junk
How to Block Bad Bots on Your Server?
Connect to your Linux server via SSH and run the following command as root:
/go/blacklist
How can I determine the source IP of a DDOS attack?
Connect to your Linux server via SSH and run the following command as root:
/go/ddos
How to import a single table from a dump file in MySQL?
Connect to your Linux server via SSH and run the following command as root:
/go/table -f file.sql -t TableName -o out.sql
mariadb DatabaseName < out.sql
How can I get the 10 most frequently executed SQL queries?
This command will return the 10 most frequently executed SQL queries.
/go/querytop
How can I get the SQL queries that are currently running on my MariaDB or MySQL server?
This will show only the active queries that are currently being executed and exclude idle connections.
/go/mysqltop
How can I monitor web server traffic in real-time on Apache?
You can use HTTPTOP to monitor web server traffic in real time. It provides an interactive, real-time view of Apache log files, displaying detailed statistics on incoming requests, traffic patterns, and server performance. This tool helps in quickly identifying high-traffic URLs, status codes, request counts, and server health.
/go/httptop
How can I change the Browser Cache TTL on Cloudflare?
To change the Browser Cache TTL on Cloudflare using the API via command line, you can use the following:
/go/cloudflare all browser 3600
How can I solve the "Too many certificates" error in Let's Encrypt?
To solve the "Too many certificates" error in Let's Encrypt using the command line, you can follow these steps:
/go/ssl all --buypass
/go/ssl all --limit
How do I migrate my database from MySQL/MariaDB to PostgreSQL?
Converting from MySQL/MariaDB to PostgreSQL
mariadb-dump database_name > db.sql
/go/mariadb2postgre db.sql
PGPASSWORD="password" psql -h localhost -U database_username -d database_name -f db.sql
