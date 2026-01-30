# Redis-Node

Installing Redis on Mac doc -

1. check if homebrew is already installed. `which brew`
2. if not, install brew from brew.sh [/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"]
3. after installation, run brew install redis
4. run `redis services start redis`
5. confirm the installation - `redis-cli ping`

Node terminal inline to play around with redis

1. In a new terminal, type `node`, this will start up a new interactive CMD with node
2. Import redis - `const redis = require('redis')`
3. Redis server by default runs on loopback address in local - `const redisUrl = `http://127.0.0.1:6379';`
4. Create a redis client - `const client = redis.createClient(redisUrl)`
5. set a KV pair into the memory of the Redis - `redis.set('hi','there');`
6. get a KV pair - `redis.get('hi', (err, val) => console.log(err,val));`
7. hash a KV Pair - `redis.hset('german', 'red','rot');`
8. get a hashed KV pair - `redis.hget('german', 'red', console.log)`
