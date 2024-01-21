- [[postgres]]
- {{embed ((65732c46-7769-41f2-ac2e-77883ebbc9f5))}}
- # How to set up the global config for postgres
- Editor of choice `sudo helix /var/lib/pgsql/data/pg_hba.conf`
  logseq.order-list-type:: number
- logseq.order-list-type:: number
  ```
  # TYPE  DATABASE        USER            ADDRESS                 METHOD
  
  # "local" is for Unix domain socket connections only
  local   all             all                                     trust
  
  ```
	- Notice the the change to **trust**
	  logseq.order-list-type:: number
- # Going through the motions of setting up a database
- Create a new database
  logseq.order-list-type:: number
  collapsed:: true
	- `createdb new_ihub_database_by_rijan`
	  logseq.order-list-type:: number
- Start the server
  logseq.order-list-type:: number
	- `sudo systemctl start postgresql.service`
	  logseq.order-list-type:: number
- Open a connection to a server
  logseq.order-list-type:: number
	- ` psql -U rijan -d new_soyabean_database_by_rijan`
	  logseq.order-list-type:: number
- Filter for an x number of rows
  logseq.order-list-type:: number
	- `SELECT * FROM your_table LIMIT 5000;`
	  logseq.order-list-type:: number
- # Things tried
- `createdb -h localhost -U rijan_dhakal sample_restore_db`
- How to enter `psql`
	- ` sudo su postgres`
- I currently get into the db using
	- ` psql -U rijan -d new_soyabean_database_by_rijan`
- `\dt` is used to list tables
-