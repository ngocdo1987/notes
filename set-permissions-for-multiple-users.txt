Set permissions for multiple users (Set permission cho nhiều users, ví dụ user apache + user đang xài Git trên server)

# do this as root
groupadd vpsusers
gpasswd -a apache vpsusers
gpasswd -a bob vpsusers   # if you have a user named bob
gpasswd -a alice vpsusers # if you have a user name alice
# etc...

# also do this as root
chown -R apache:vpsusers /your/directory

# again, as root
chmod -R g+w /your/directory
