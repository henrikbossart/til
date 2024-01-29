# When postgres is updated
1. Delete the postmaster.pid file:
    ```
    rm /usr/local/var/postgres/postmaster.pid
    ```
2. Restart your postgres:
    ```
    brew services restart postgresql
    ```


For M1 Mac you would replace stage 1 with:
```
rm /opt/homebrew/var/postgresql/postmaster.pid
```

With M1 and specify Postgres Version @ 14
```
rm -rf /opt/homebrew/var/postgresql@14/postmaster.pid
```
