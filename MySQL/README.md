# Install MySQL on ubuntu

Update apt-get
```
sudo apt-get update
```
Install mysql using apt-get
```
sudo apt-get install mysql-server -y
```
Start MySQL Service
```
sudo systemctl start mysql.service
```
To Configure MySQL
```
sudo mysql_secure_installation
```
Check MySQL
```
sudo mysql
```
To change the root user password
```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'your_password';
```
To create a new user 

* Login into mysql

```bash
sudo mysql -u root -p
```
```
CREATE USER 'your_user'@'localhost' IDENTIFIED WITH authentication_plugin BY 'your_password';
```
or 
```
CREATE USER 'user'@'localhost' IDENTIFIED BY 'your_password';
```

To Grant all privilege to user 
```
GRANT ALL PRIVILEGES ON *.* TO 'user_name'@'localhost' WITH GRANT OPTION;
```
```
FLUSH PRIVILEGES;
```


