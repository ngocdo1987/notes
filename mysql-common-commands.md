0/ Setup remote connection
On database server
sudo ufw allow from <php-server-ip> to any port 3306
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf

Change
bind-address            = <mysql-server-ip>
mysqlx-bind-address     = <mysql-server-ip>

1/ Add new user and grant for new DB
CREATE DATABSE zein_mochida;
CREATE USER 'zein'@'<php-server-ip>' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON zein_mochida.* TO zein@'<php-server-ip>';
FLUSH PRIVILEGES;
