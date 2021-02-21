### Install postgres from binaries


[Download Here!](https://www.enterprisedb.com/download-postgresql-binaries)

Extract...... :thumbsup:

in `.bash_profile` or `.zshrc`

```bash
# Postgres config
export PATH="$HOME/dev/pgsql/bin:$PATH"

export PGLOGFILE="$HOME/dev/pgdata/postgres.log"
export PGDATA="$HOME/dev/pgdata"

alias start_postgres="pg_ctl -D ${PGDATA} -l ${PGLOGFILE} start"
alias stop_postgres="pg_ctl -D ${PGDATA} -l ${PGLOGFILE} stop"	
```

##### InitDB (create database folder structure)

```bash
initdb ${PGDATA}
```

##### Create user/role

```bash
createuser --interactive --pwprompt
	Enter name of role to add: <user>
	Enter password for new role:
	Enter it again:
	Shall the new role be a superuser? (y/n)
```

##### Create database

```bash
createdb -O <user_name> <db_name>
```

##### Login to database

```bash
psql -U <user_name> -d <database> -h <host> -p <port> -a
```

##### Drop user/role

```vim
drop user <user_name>
```

