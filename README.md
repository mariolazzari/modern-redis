# Modern Redis

## Setup

### Redis stack in cloud

[redis.io](https://redis.io/)
[Redis cloud](https://cloud.redis.io/)

```sh
redis-cli -h hostname -p port -a password
info
ping
exit
```

### Simple cache operations

```sh
# single key
SET foo bar
GET foo
# multiple keys
MSET jupiter planet sun star
MGET jupiter sun
# hash
HSET captains enterprise kirk
HGET captains enterprise
HSET captains voyager mario
HGET captains voyager
# left push
LPUSH ships enterprise
LPUSH ships voyager
# right pop
RPOP ships
RPOP ships
```
