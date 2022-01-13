\#cache

# Caching

## General

Caching may be implement at diffrent places; at the client(ex webbrowser) , local proxy server , server side reverse proxy or as part of API gateway. 

Stale is a state when the expiration time has expired for the cache. 

Check if cache is expering when the state is "Stale"  and need to be validated if the cache is still up to date. 
Validate method : 

Date/timestamp : Last-Modified Header. 
ETag : revision number or hash of the content in a ETag header. 
