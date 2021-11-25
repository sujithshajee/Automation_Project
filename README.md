# Automation_Project

## Description
The bash script is used to perform below activities on the Ubuntu server.

```bash
Updates the package information
Ensures that HTTP Apache server is installed
Ensures that HTTP Apache server is running
Ensures that HTTP Apache service is enabled
Archiving HTTP Server logs from /var/log/apache2/ to S3
Sets up cronjob to archive log files on daily at midnight
Creates and records historical data of archival at location /var/www/html/inventory.html
```

## Prerequisites
Ensure below requirements fulfilled on server

```bash
  Ubuntu Server 18.04 LTS (HVM)
  Bash configured
  AWS CLI configured - Refer link for details https://linuxhint.com/install_aws_cli_ubuntu/ 
```


## Usage

```bash
Clone the repo on server
Update below variables with appropriate values by editing automation.sh
  #update the variable with the s3 bucket name in aws
  s3_bucket="upgrad-sujithshajee"
  #provide the prefix that needs to be used to archive file on s3 bucket
  fileprefix="sujith"
Provide execute permission on the automation.sh file running below command
  sudo su
  chmod 755 automation.sh
Execute the script using following command
  ./automation.sh
```