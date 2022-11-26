# Description

This role deploys [Ergo](https://ergo.chat/), an IRC server written in Go.

# Configuration

A minimal configuration would require:
```yaml
ergo_network_name: 'ExampleOrg'
ergo_server_name: 'irc.example.org'
ergo_message_of_the_day: 'Welcome to Example.org IRC server!'
ergo_history_autoresize_window: 14d
ergo_max_concurrent_conns: 128
ergo_cont_certs_vol: '/certs/example.org'
ergo_server_password: '$2a$04$...'
ergo_admin_password: '$2a$04$...'
```

# Management

Serivce is managed using [Docker Compose](https://docs.docker.com/compose/):
```
 > docker-compose ps
Name              Command               State                        Ports                      
------------------------------------------------------------------------------------------------
ergo   /ircd-bin/ergo run --conf= ...   Up      127.0.0.1:6667->6667/tcp, 0.0.0.0:6697->6697/tcp
```

# Administration

For general usage and admin docs see [`USAGE.md`](./USAGE.md).

For more info see [the oficial manual](https://github.com/ergochat/ergo/blob/stable/docs/MANUAL.md).
