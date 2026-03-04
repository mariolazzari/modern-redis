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

## PubSub and streaming

### PubSub

```sh
SUBSCRIBE ch1
PUBLISH ch1 ciao
```

### Straming

- Appended infinetly
- Logs data
- Consumers can query ranges
- Just listen fon new items

```sh
# XADD mystream * field1 value1 field2 value2 -> * autogen id
XADD orders * user_id 42 total 99.50 status pending
```

## Storing data

### RedisJSON

- horizontal scalable nosql
- update individual field

```sh
JSON.SET enterprise . '{"captain": "kirk"}'
JSON.GET enterprise
```

#### Redis object mapping

- native data structure

### RediSearch

- indexing and querying
- full-text and fuzzy search

## Time series

### ReidsTimeSeries

- query for start and end times
- aggregations
- retention period
- indexed labels
- integrations

## RedisGraph

### deprecated
