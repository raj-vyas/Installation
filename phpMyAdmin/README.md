# Install phpMyAdmin on ubuntu

Update apt-get
```
sudo apt-get update
```
Install phpmyadmin and php packages
```
sudo apt-get install phpmyadmin php-mbstring php-zip php-gd php-json php-curl
```
Select apache2

* Click on the spacebar and then click on the tab and then Ok.

```
sudo phpenmod mbstring
```
Restart Apache
```
sudo systemctl restart apache2
```
Start MysQl
```
sudo mysql
```
or 
```
sudo mysql -u root -p
```
Create new user 
```
CREATE USER 'raj'@'localhost' IDENTIFIED WITH caching_sha2_password BY 'your_password';
```
if this does not work then run this alter command 
```
ALTER USER 'raj'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
Grant all privileges to the user 
```
GRANT ALL PRIVILEGES ON *.* TO 'raj'@'localhost' WITH GRANT OPTION;
```
```
FLUSH PRIVILEGES;
```
```
EXIT;
```

To Run PHPMyAdmin

http://localhost/phpmyadmin



