Sometimes postgres decides to act like shit.

Remove the `postmaster.pid` file and restart the service.

```bash
rm /opt/homebrew/var/postgresql@14/postmaster.pid
brew services restart postgresql@14
```