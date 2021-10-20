# Postgres HELP

## Install postgres from binaries

[Download binaries from here!](https://www.enterprisedb.com/download-postgresql-binaries)

## Install postgres from source

- [Download sources from here!](https://www.postgresql.org/ftp/source/)
  ```shell
  # Extract the source
  tar -xvzf postgresql-<VERSION>.tar.gz
  cd postgresql-<VERSION>
  ```
- Clone from git, [check tags here!](https://git.postgresql.org/gitweb/?p=postgresql.git;a=tags)
  ```shell
  # Clone the repo
  git clone --depth 1 -b <TAG> https://git.postgresql.org/git/postgresql.git
  cd postgresql
  ```
- Make and Install
  ```shell
  # Check openssl
  which openssl
  
  # Configure the build
  ./configure --with-openssl \
    --with-includes=/usr/local/opt/openssl/include \
    --with-libraries=/usr/local/opt/openssl/lib 
    --prefix $HOME/dev/postgres/pgsql
  
  # Make
  make world
  
  # Install
  make install-world 
  ```

## Configure

### env variables and aliases

```shell
# Postgres config
export PGHOME="$HOME/dev/postgres"
export PGLOGFILE="$PGHOME/postgres.log"
export PGDATA="$PGHOME/pgdata"

export PATH="$PGHOME/pgsql/bin:$PATH"

alias start_postgres="pg_ctl -D ${PGDATA} -l ${PGLOGFILE} start"
alias stop_postgres="pg_ctl -D ${PGDATA} -l ${PGLOGFILE} stop"
```

### InitDB (create database folder structure)

```shell
initdb ${PGDATA}
```

### Create user/role

```shell
createuser --interactive --pwprompt
```

### Create database

```shell
createdb -O <user_name> <db_name>
```

### Login to database

```shell
psql -U <user_name> -d <database> [-h <host>] [-p <port>] -a
```
