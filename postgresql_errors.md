### Failiure to start

[See StockOverFlow](http://stackoverflow.com/questions/19828385/pgconnectionbad-could-not-connect-to-server-connection-refused)

> FATAL:  lock file "postmaster.pid" already exists
> HINT:  Is another postmaster (PID 347) running in data directory "/usr/local/var/postgres"?

#Remove postgre socket id
`$ rm /usr/local/var/postgres/postmaster.pid`

then

0. `$ brew info postgresql`
1. `$ cd /usr/local/var/postgres`
2. `$ rm postmaster.pid`
3. `$ launchctl unload ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist`
4. `$ launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist`
