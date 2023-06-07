[Link](https://stackoverflow.com/questions/24718706/backup-restore-a-dockerized-postgresql-database)

# Steps to dump DB
## Create dump by date
```
sudo docker exec -t #DB_NAME# pg_dumpall -c -U user > dump_`date +%Y-%m-%d"_"%H_%M_%S`.sql
```
## (Optional) Create another DB
`sudo docker run --name #DB_NAME# -p 1234:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres`

# Schedule task
[link](https://stackoverflow.com/questions/51649484/how-to-backup-postgresql-database-automatically-on-daily-basis)
## Create bash file
Create a file with name `backup.sh`
- `nano backup.sh`
- enter 
```
  #!/bin/bash
  sudo docker exec -t #DB_NAME# pg_dumpall -c -U user > dump_`date +%Y-%m-%d"_"%H_%M_%S`.sql
```
- run command `crontab -e`
- add entry `0 1 * * *   ./backupDB.sh`

# Restore the db
`cat dump_2023-06-07_18_29_16.sql | docker exec -i #DB_NAME# psql -U postgres`
- `-U` user
- `some-postgres` DB name
