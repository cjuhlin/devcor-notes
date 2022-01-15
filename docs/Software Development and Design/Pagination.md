\#pagination

# Pagination

## Pros with paginations

Improving response times

Saving resource because smaller payloads 

## Different types

### Offset/Page

The client can use  `offset=` and `limit=`   example 

````
https://exampel.com/article?offset=100&limit=20
````

Will return 20 entries starting from 100. 

#### Cons

Problem if entries get added or deleted. So if an entries get deleted on some page it will cause entries to move to the previous page instead. It called page drift.

When dealing with large offset the API would scan through all of the offset and discard them.

### Cursor- or keyset

Use some "key" value to indicate an starting item. Like dates. This  will solve the problem that [Offset Page](Pagination.md#offset-page) has.

Example

````
https://exampel.com/article?max=20&before=2022-01-14
````

Will get 20 entries before 2022-01-14 

### Metadata

Another way is for the API to return metadata with information about pagination 

Example:

````
https://example.com/fruits
````

returns :

````
"items": ["Apple","Banana","Orange"],
"paging": {
	"offset" : 0,
	"limit" : 3,
	"count" : 42,
	"prev" : []
	"next" : ["https://example.com/fruits?offset=4&limit=3",xxxx,xxxx,xxxx],
	"pages" : 14
}
````
