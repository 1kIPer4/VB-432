### PSR-6: Caching Interface
## Definitions
- **Calling Library** - The library or code that actually needs the cache services. This library will utilize caching services that implement this standard's interfaces, but will otherwise have no knowledge of the implementation of those caching services.
- **Implementing Library** - This library is responsible for implementing this standard in order to provide caching services to any Calling Library. The Implementing Library MUST provide classes which implement the Cache\CacheItemPoolInterface and Cache\CacheItemInterface interfaces. Implementing Libraries MUST support at minimum TTL functionality as described below with whole-second granularity.
- **TTL** - The Time To Live (TTL) of an item is the amount of time between when that item is stored and it is considered stale. The TTL is normally defined by an integer representing time in seconds, or a DateInterval object.
More PSR6 info [link](https://www.php-fig.org/psr/psr-6/)
# CacheException
Any exception thrown by an Implementing Library MUST implement this interface.
```
<?php

namescape Psr\Cache;

interface CacheException
{
}
```
Key Concepts
POOL | The Pool represents a collection of items in a caching system. The pool is a logical Repository of all items it contains. All cacheable items are retrieved from the Pool as an Item object, and all interaction with the whole universe of cached objects happens through the Pool
ITEMS | An Item represents a single key/value pair within a Pool. The key is the primary unique identifier for an Item and MUST be immutable. The Value MAY be changed at any time.

