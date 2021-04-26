# JS File search

Imagine that you have a very long list of file paths (path_list)
that it is updated once a day.
 
You need to make a function to search for the existence of files or folders
in the path_list. Those files or folders come in the form of another list (search_items).
The function will run thousands of times per minute, so
you must implement an algorithm resistant to the challenge situation.
Some cases and the expected results are detailed in the search_items list.
 
Tips & rules:
- You cannot use regex
- All entries in path_list will start with " / "
- A wildcard may be present for the items to be searched " * "
- All paths and filenames come free of error and Unix like

```js
const path_list = [
    "/usr/bin",
    "/var/cache/apache2/mod_cache_disk",
    "/usr/bin/wget",
    "/usr/bin/curl",
    "/var/cache/apache2",
];

const search_items = [
    "/usr", //true
    "/usr/bin", //true
    "/usr/bins", //false
    "/usr/var", // false
    "/var/cache/*/mod_cache_disk", //true
    "/*/*/wget", //true
    "/*/*/postman", //false
    "/var/cache/nginx", //false
    "/*/bin", //true
];

```
