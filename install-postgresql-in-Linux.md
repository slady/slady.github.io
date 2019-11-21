# Install PostgreSQL server in Linux
If you are using Debian or Ubuntu Linux, install postgresql:
`sudo apt install postgresql`

If you run Fedora, run `yum` or any other command on your respective variant of Linux.

To start, stop or restart:
sudo service postgresql restart

# Add user
To create a database user in PostgreSQL, we need to create a real user in the system:
`sudo adduser <<username>>`

# Create database
First login as `postgres` user in Linux:
`sudo -u postgres -i`

```
createuser <<username>>
createdb <<dbname>>
psql <<dbname>>
dbname=# alter user <<username>> with password 'mySecretPassword';
^D
```
