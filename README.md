##ckan-purger


This is a process for purging the data from CKAN installation.

Curently it removes (**hard delete**) all the datasets and organizations.

## Requirements

* Unix environment (tested on Ubuntu 12.04 and OS X, should work with Cygwin on Windows)

## Configuration
Create a file `settings.py`, which will include configuration values:

- the API location of the CKAN isntance to harvest into,
- the API key of a the CKAN instance

Example:

```
CKAN_API_PATH = "http://localhost:5000/api/3/"
API_KEY = "199d2a0b-5e24-4c1e-bfbb-21f8692f2f79"
```

## Running the purger

`python purge.py`

This will **hard delete** the datasets and the organizations.

## Limitations

- There is no progress logging. The scripts operate silently. This makes it a bit hard to understand what exactly they are doing.
- Error reporting/handling is very basic.

