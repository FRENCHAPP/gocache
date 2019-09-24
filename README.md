[![Build Status](https://semaphoreci.com/api/v1/brad/gocache/branches/master/shields_badge.svg)](https://semaphoreci.com/brad/gocache)
[![codecov](https://codecov.io/gh/rubanbydesign/gocache/branch/master/graph/badge.svg)](https://codecov.io/gh/rubanbydesign/gocache)

Cache is a package which implements a unified interface for various Golang based cache.

Current drivers include:

- In-memory LRU cache  [github.com/rubanbydesign/gocache/drivers/lru](https://godoc.org/github.com/rubanbydesign/gocache/drivers/lru)
- [memcached](https://godoc.org/github.com/bradfitz/gomemcache/memcache)
- Redis via [redigo](https://godoc.org/github.com/garyburd/redigo/redis)
- [github.com/patricknm/go-cache](https://godoc.org/github.com/patricknm/go-cache)
- [App Engine memcache](https://godoc.org/google.golang.org/appengine/memcache)
- [Go-radix](https://godoc.org/github.com/armon/go-radix)
- [FreeCache](https://godoc.org/github.com/coocood/freecache)
- [BigCache](https://godoc.org/github.com/allegro/bigcache)
- [Golang-lru](https://godoc.org/github.com/hashicorp/golang-lru)
- A bridge driver to [github.com/rubanbydesign/gokv]((https://godoc.org/github.com/rubanbydesign/gokv) which can implement
  anything which implements the `kv.Store` interface, currently including:
    - [AppEngine datastore](https://godoc.org/github.com/rubanbydesign/gokv/drivers/appengine/datastore)
    - [BoltDB](https://godoc.org/github.com/rubanbydesign/gokv/drivers/boltdb)
    - [DiskV](https://godoc.org/github.com/rubanbydesign/gokv/drivers/diskv)
    - [LevelDB](https://godoc.org/github.com/rubanbydesign/gokv/drivers/level)

More drivers are most welcome! Just make sure they meet at least the `"cache".Cache`
interface and are unit tested.
