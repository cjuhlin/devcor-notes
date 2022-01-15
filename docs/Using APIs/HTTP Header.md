# HTTP header

## Headers

### Cache-Control

Often use cache headers. 

#### no-store

The response may not be stored in any cache

#### no-cache

Allow caching but stored response need to be validated first before use. 

#### max-age

Time in seconds a cached copy is valid.

#### public

Can be cached by anyone.

#### private

Only browser/client may cache.

### Example

````
Cache-Control: no-cache, max-age=10
````
