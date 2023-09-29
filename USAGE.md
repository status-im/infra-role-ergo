# Description

This describes how to perform basic tasks of IRC server as user and adminiastrator.

# Usage

## User Registration

If registration is not enabled via `accounts.registration.enabled` you can use:
```
/msg nickserv register <password> joe@example.org
```
Password can be changed using:
```
/msg nickserv passwd <current> <new_pass> <new_pass_again>
```

## Be Always Visible

To remain visible on the server even when you are disconnected use:
```
/msg NickServ set always-on true
```

# Administration

## Channel Creation

First you have to join a channel you want to register:
```
/join #newchannel
```
But that kind of channel is ephemeral and will disappear once all users leave it.

As operator you can register the channel to be permanent:
```
/msg ChanServ register #newchannel
```
