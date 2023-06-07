[Link](https://stackoverflow.com/questions/24718706/backup-restore-a-dockerized-postgresql-database)

# Steps to dump DB
```
sudo docker exec -t db-my pg_dumpall -c -U user > dump_`date +%Y-%m-%d"_"%H_%M_%S`.sql
```
# (Optional) Create another DB
`sudo docker run --name some-postgres -p 1234:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres`
# Restore the db
`cat dump_2023-06-07_18_29_16.sql | docker exec -i some-postgres psql -U postgres`
- `-U` user
- `some-postgres` DB name
