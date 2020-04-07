## pgformatter

Thin Python wrapper for [pgFormatter](https://github.com/darold/pgFormatter/).
Compatible with AWS Lambda or any environment with Perl.

```python
from pgformatter import pg_format

pg_format(
    b"""
SELECT f.title, f.did, d.name, f.date_prod, f.kind
    FROM distributors d, films f
    WHERE f.did = d.did
"""
)
```

```sql
SELECT
    f.title,
    f.did,
    d.name,
    f.date_prod,
    f.kind
FROM
    distributors d,
    films f
WHERE
    f.did = d.did
```
