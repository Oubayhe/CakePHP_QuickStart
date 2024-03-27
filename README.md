# Quick Start CakePHP
- Before starting make sure you have php installed by entering this in your terminal
```
php -v
```
- Also in my case I'm using XAMP.
- All the commands that we're going to be used, are prefered to be emplemented in the same directory.
## 1. Install Composer:
To install just enter these commands in the termianl:
```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'dac665fdc30fdd8ec78b38b9800061b4150413ff2e3b6f88543c636f7cd84f6db9189d43a81e5503cda447da73c7e5b6') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
## 2. Enable extension:
In your php.ini file (C:\php-8.3.2\php.ini) you should uncomment **extension=php_intl.dll (or extension=intl)**
## 3. Create a CakePHP project:
Enter this command to the termianl, with my_app_name being the name you want to give for this project:
```
php composer.phar create-project --prefer-dist cakephp/app:5.* my_app_name

```
> [!IMPORTANT]
> If you had problem creating the app, make sure that you've actually uncommented **extension=php_intl.dll (or extension=intl)** in C:\php-8.3.2\php.ini, and in C:\xampp\php\php.ini
## 4. View the created project:
* Enter to the created project directory:
```
cd my_app_name
```
* Run the project:
```
bin/cake server
```
* copy the built-in server link (example:http://localhost:8765/)
> [!IMPORTANT]
> You might face this Error message: **Database driver `Cake\Database\Driver\Sqlite` cannot be used due to a missing PHP extension or unmet dependency. Requested by connection  `test`**.
> to solve you go to php.ini, and uncomment **extension=pdo_sqlite**
## 5. Connect to the database:
* Create a database in your phpMyAdmin
* In you project folder go to **config/app_local.php** and set the username, password and database to thier actuall values.
