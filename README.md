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
```
