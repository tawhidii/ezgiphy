# ezgiphy 0.0.4

#### A wrapper for the Giphy public API.
A package wrapper for the Giphy public API that allows you to work with all Giphy API endpoints.



Installing using pip
```
pip install ezgiphy
```

### Examples (Giphy public api endpoints)

```python
from ezgiphy import GiphyPublicAPI

giphy = GiphyPublicAPI('<giphy-api-key>')

```
#### Phrase search
Search all Giphy GIFs for a word or phrase. Supported parameters:
- q : Search query term or phrase (required).
- limit :  The maximum number of records to return.
- offset: An optional results offset.
- rating: Filters results by rating (g/pg/pg-13/r)
- lang: specify default country for regional content.

```python
giphy.search(q='something',limit=25,rating='g')
```

#### Translate search
Experimental search endpoint for gif dialects. Supported parameters:
- s : Search query term or phrase (required).

```python
giphy.translate(s='something')
```

#### Trending gifs
Get all trending gifs. Supported parameters:

- limit: The maximum number of records to return. 
- rating: Filters results by rating (g/pg/pg-13/r),

```python
giphy.trending(limit=25,rating='g')
```

#### Random gifs
Random gif(s) filtered by tag. Supported parameters:

- tag: The maximum number of records to return.
- rating: Filters results by rating (g/pg/pg-13/r).
```python
giphy.random(tag='something',rating='g')
```
#### Giphy Id search
Search Giphy gifs for a single Id. Supported parameters:

- id: Filter result by specific gif id (required).

```python
giphy.get_by_id(id='some id')
```

#### Search by ids 
Search all Giphy gifs for  an list of Id's. Supported parameters:

- ids: List of specific ids (required).
```python
giphy.get_by_ids(ids=['id one','id two','id three'])
```


### Examples (Giphy sticker api endpoints)

```python
from ezgiphy import GiphyStickerAPI

sticker =  GiphyStickerAPI('<giphy-api-key>')

```
#### Phrase search
Search all Giphy Stickers for a word or phrase. Supported parameters:
- q : Search query term or phrase (required).
- limit :  The maximum number of records to return.
- offset: An optional results offset.
- rating: Filters results by rating (g/pg/pg-13/r)
- lang: specify default country for regional content.

```python
sticker.search(q='something',limit=25,rating='g')
```

#### Translate search
Experimental search endpoint for sticker dialects. Supported parameters:
- s : Search query term or phrase (required).

```python
sticker.translate(s='something')
```

#### Trending gifs
Get all trending stickers. Supported parameters:

- limit: The maximum number of records to return. 
- rating: Filters results by rating (g/pg/pg-13/r),

```python
sticker.trending(limit=25,rating='g')
```

#### Random gifs
Random sticker(s) filtered by tag. Supported parameters:

- tag: The maximum number of records to return.
- rating: Filters results by rating (g/pg/pg-13/r).
```python
sticker.random(tag='something',rating='g')
```
#### Giphy Id search
Search Giphy stickers for a single Id. Supported parameters:

- id: Filter result by specific gif id (required).

```python
sticker.get_by_id(id='some id')
```


#### Search by ids 
Search all Giphy sticker for  an list of Id's. Supported parameters:

- ids: List of specific ids (required).
```python
sticker.get_by_ids(ids=['id one','id two','id three'])
```