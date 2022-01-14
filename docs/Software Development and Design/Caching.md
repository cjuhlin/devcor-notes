\#cache

# Caching

## General

Caching may be implemented at different places; at the client(ex web-browser), local proxy server, server-side reverse proxy, or as part of API gateway. 

Stale is a state when the expiration time has expired for the cache. 

Check if the cache has expired when the state is "Stale"  and needs to be validated if the cache is still up to date. 
Validate method : 

Date/timestamp: Last-Modified Header. 
ETag: revision number or hash of the content in an ETag header. 
