Start docker
===
docker run --name node-postgres-dev -p 5432:5432 -d -e POSTGRES_PASSWORD=password postgres:15 -c ssl=on -c ssl_cert_file=/etc/ssl/certs/ssl-cert-snakeoil.pem -c ssl_key_file=/etc/ssl/private/ssl-cert-snakeoil.key

After it starts
===
docker exec node-postgres-dev /bin/bash -c "createdb -U postgres test"

Depending on your env
===
```
set PGHOST=127.0.0.1
set PGPORT=5432
set PGDATABASE=test
set PGUSER=postgres
set PGPASSWORD=password
```

```
export PGHOST=127.0.0.1
export PGPORT=5432
export PGDATABASE=test
export PGUSER=postgres
export PGPASSWORD=password
```

```
Set-Variable -Name "PGHOST" -Value "127.0.0.1"
Set-Variable -Name "PGPORT" -Value "5432"
Set-Variable -Name "PGDATABASE" -Value "test"
Set-Variable -Name "PGUSER" -Value "postgres"
Set-Variable -Name "PGPASSWORD" -Value "password"
```

```
$env:PGHOST = '127.0.0.1';
$env:PGPORT = '5432';
$env:PGDATABASE = 'test';
$env:PGUSER = 'postgres';
$env:PGPASSWORD = 'password';
```