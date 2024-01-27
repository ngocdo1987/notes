Linux: How to Send Mail From Command Line Using SMTP Server

1/ sudo apt-get install ssmtp

2/ sudo vim /etc/ssmtp/ssmtp.conf
Edit the above file with the below details:

mailhub=smtp.gmail.com:587
useSTARTTLS=YES
AuthUser=username-here
AuthPass=password-here
TLS_CA_File=/etc/pki/tls/certs/ca-bundle.crt

3/ Bash script file
#!/bin/sh  
SUBJECT="Test Subject"
TO="crazy@yopmail.com"
MESSAGE="Hey There! This is a test mail"

echo $MESSAGE | sudo ssmtp -vvv $TO

sudo chmod 755 mail.sh
sudo ./mail.sh

*** Detail: https://netcorecloud.com/tutorials/linux-send-mail-from-command-line-using-smtp-server/
