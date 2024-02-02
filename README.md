# Setting Up MySQL Database

This guide will walk you through the process of setting up a MySQL database with a new user using the command line.

## Prerequisites

- MySQL installed on your system

## Steps

1. Open your terminal or command prompt.

2. Log in to MySQL as the root user:

   ```bash
   mysql -u root -p
   use mysql
   CREATE USER 'Put your new user name here'@'%' IDENTIFIED BY 'Put your new password here';
   GRANT ALL PRIVILEGES ON *.* TO 'Put your new user name here'@'%' WITH GRANT OPTION;
   FLUSH PRIVILEGES;
   exit
   
Output:

![](https://media.discordapp.net/attachments/949506107615879178/1203065362271436851/how_to_set_up_db_3-23_screenshot.png?ex=65cfbcee&is=65bd47ee&hm=2eee5c727aa0be5010e1f9bbe8eb5561d818f9d28592fb5c9374df810e75fb30&=&format=webp&quality=lossless)


> [!NOTE]
> You Need To Open The ports for the MySql which is 3306.

- This is to be done when you are not able to add the data in the panel.
- Make sure your MYSQL Ports are open.

1. You need to go in this file
```bash
nano /etc/mysql/mariadb.conf.d/50-server.cnf
```

4. Change the Bind port from ``127.0.0.1`` TO ``0.0.0.0``


- **Don't use the numpad of your keyboard in this file.**

4. Save the file.

5. Run
```bash
   systemctl restart mysql && systemctl restart mariadb
```
- So that all the settings take place
